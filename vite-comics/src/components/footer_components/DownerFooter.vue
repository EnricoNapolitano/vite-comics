<script></script>
<template>
    <footer>
        <!-- Here starts the footer downside -->
        <div class="row container">
            <button>SIGN-UP NOW!</button>
            <div>
                <span>FOLLOW US</span>
                <!-- ICONS, TO DO -->
                <i>F</i>
                <i>F</i>
                <i>F</i>
                <i>F</i>
                <i>F</i>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partial/variables' as *;
@use '../../assets/scss/partial/mixins.scss' as *;

// GRAPHICS TO DO
footer {
    background-color: $grey;
}

div.row {
    height: 110px;
    @include flex-jsb-ac;
}
</style>