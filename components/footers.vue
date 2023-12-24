<template>
    <div class="background">
        <div class="columns">
            <div>
            <p>f</p>
            <p>f</p>
        </div>
        <div>
            <p>f</p>
            <p>f</p>
        </div>
        <div>
            <p>f</p>
            <p>f</p>
        </div>
        </div>
    </div>
</template>
<style scoped>
.background {
    background-color: black
}
.columns {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    column-gap: 10px;
}
h2,p {
    color: white
}
</style>