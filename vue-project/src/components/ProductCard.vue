<template>
<div class="product-card">
    <img :src="image" alt="Product Image">
    <h3 v-html="formattedTitle"></h3>
    <div class="prices">
    <div class="discount-price">{{ formattedDiscountPrice }}</div>
    <div class="price-line">
        <span class="normal-price">{{ formattedNormalPrice }}</span>
        <span class="discount-tag">{{ discountTag }}</span>
    </div>
    </div>
    <button @click="addToBag">Add to Bag</button>
</div>
</template>

<script>
export default {
props: ['title', 'image', 'discount', 'normal', 'discountPrice'],
computed: {
formattedTitle() {
    const maxCharactersPerLine = 21; // Adjust the character limit as needed
    const lines = this.title.split(' ');
    let currentLine = lines[0];
    let result = '';

    for (let i = 1; i < lines.length; i++) {
    const testLine = currentLine + ' ' + lines[i];
    if (testLine.length <= maxCharactersPerLine) {
        currentLine = testLine;
    } else {
        const secondLine = lines.slice(i).join(' ');
        result = currentLine + '<br>' + secondLine.slice(0, maxCharactersPerLine);
        if (secondLine.length > maxCharactersPerLine) {
            result += '...';
        }
        break;
    }
    }

    return result;
},
formattedDiscountPrice() {
    return `${this.formatCurrency(this.discountPrice)}`;
},
formattedNormalPrice() {
    return `${this.formatCurrency(this.normal)}`;
},
discountTag() {
    return `${this.discount}%`;
}
},
methods: {
    addToBag() {
    alert('Product added to bag!');
    // Add your logic for adding the product to the shopping bag
    },
    formatCurrency(value) {
    return new Intl.NumberFormat('id-ID', {
        style: 'currency',
        currency: 'IDR'
    }).format(value);
    }
}
};
</script>

<style scoped>
.product-card {
    width: 182px;
    text-align: center;
    margin: 10px;
    margin-top: 20px;
    background-color: #ffffff;
    padding: 10px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5); /* Adjust the shadow as needed */
}

@media screen and (max-width: 960px) {
    .product-card {
        width: 132px;
    }
}

.product-card img {
    max-width: 100%;  /* Set the maximum width to the container width */
    height: auto;
    max-height: 150px;
}


.product-card h3 {
    font-size: 14px;
    margin: 5px 0;
    white-space: pre-line;
    overflow: hidden;
    text-overflow: ellipsis;
    color: #000000;
    text-align: left; /* Set text alignment to left */
    font-weight: 600; /* Semi-bold font weight */
}


.prices {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-top: 8px;
    margin-bottom: 8px;
}

.price-line {
    display: flex;
    align-items: center;
    gap: 2px; /* Add 2px of space between items */
    width: 100%;
}

.discount-price {
    font-size: 16px;
    color: orange;
    font-weight: 600; /* Semi-bold font weight */
}


.normal-price {
    font-size: 12px;
    color: #808080; /* Grey color */
    font-weight: 500;
}

.discount-tag {
    background-color: #ffb6c1; /* Light red background */
    color: #ff0000; /* Red text color */
    padding: 2px 6px;
    font-size: 12px;
    border-radius: 16px; /* Rounded corners */
}

.product-card button {
    background-color: #0094da;
    color: #fff;
    padding: 8px;
    border: none;
    cursor: pointer;
    width: 100%;
    border-radius: 8px; /* Rounded corners */
    font-weight: 600;
}

</style>  