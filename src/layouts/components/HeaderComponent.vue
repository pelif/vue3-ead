<template>
    <div>
        <header id="header">
            <nav>
                <span class="toggleMenu far fa-bars"></span> 
                <span class="logo">
                    <img :src="require('@/assets/images/logo.svg')" alt="Especializa TI">
                </span>
            </nav>
        </header>
    </div>
</template>

<script> 
export default {
    name: 'header-component'
}
</script>