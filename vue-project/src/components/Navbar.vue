<template>
<header class="navbar">
    <div class="logo">
    <img alt="BliBli Logo" src="/BliBli-logo.png" width="125" height="125" />
    </div>
</header>
</template>

<script>
export default {
};
</script>

<style scoped>
/* Add your styling for the navbar */
.navbar {
    background-color: #0072ff; /* Set the background color of the navbar */
    padding: 10px; /* Add some padding for spacing */
    color: white; /* Set the text color to white */
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000; /* Set z-index to ensure it's above other elements */
}

@media screen and (max-width: 960px) {
  .navbar {
    justify-content: center;
  }
}

.logo img {
    width: 120px; /* Adjust the width as needed */
    height: auto; /* Maintain aspect ratio */
    margin-left: 24px;
}
</style>