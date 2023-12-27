<template>
<footer class="footer">
    <div v-show="isVisible" class="content">
        <p>This is the content to be shown or hidden.</p>
    </div>
    <button @click="toggleVisibility">{{ buttonText }}</button>
    <button @click="scrollToTop" class="scroll-up-button">
      &#9650;
    </button>
    <p class="copyright">2022 PT Global Digital Niaga</p>
</footer>
</template>
  
<script>
export default {
data() {
    return {
        isVisible: false,
    };
    },
    computed: {
        buttonText() {
            return this.isVisible ? 'Collapse All' : 'Show All';
        },
    },
    methods: {
        toggleVisibility() {
            this.isVisible = !this.isVisible;
        },
        scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        },
    },
};
</script>

<style scoped>
/* Add your styling for the footer */
.footer {
    background-color: #d3d3d3; /* Grey background color */
    padding: 20px; /* Add some padding for spacing */
    position: relative;
    text-align: center;
    bottom: 0;
    left: 0;
    right: 0;
}

button {
    color: #0094da; /* Blue text color */
    cursor: pointer;
    border: none;
    background: none;
    font-size: 16px;
    font-weight: 600; /* Semi-bold font weight */
}

.content {
    margin-top: 10px; /* Add margin to separate the content from the button */
    color: #000000; /* Black text color */
}

.copyright {
    color: #000000; /* Black text color */
    margin-top: 10px;
    font-size: 14px;
    font-weight: 600; /* Semi-bold font weight */
}

.scroll-up-button {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: #fff; /* Blue background color */
    color: #0094da; /* White text color */
    border: none;
    border-radius: 50%; /* Make it circular */
    padding: 10px;
    font-size: 16px;
    cursor: pointer;
}

.scroll-up-button i {
    /* Style the arrow icon */
    transform: rotate(-90deg); /* Rotate the arrow to point upwards */
}
</style>

