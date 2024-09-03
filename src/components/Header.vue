<script setup>

</script>

<template>
    <header>
        <div class="logo">Logo</div>
        <nav>
            <ul>
                <li>Home</li>
                <li>Concept</li>
                <li>Contact</li>
                <li>Profile</li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss">
header {
    height: 100px;
    background: rgba(220, 20, 60, 0.322);
    width: 100%;
    display: flex;
    justify-content: space-between;
    padding: 0 30px;
    align-items: center;
    .logo {
        font-size: 24px;
        font-weight: bold;
        color: crimson;
    }
    nav {
        display: flex;
        ul {
            list-style: none;
            display: flex;
            gap: 12px;
            li {
                cursor: pointer;
                color: crimson;
                &::after {
                    content: '';
                    width: 0%;
                    background: black;
                    position: absolute;
                    height: 1px;
                    bottom: 0;
                    left: 0;
                    transition: ease-out .3s;
                }
                &:hover {
                    color: black;
                    position: relative;
                    transition: ease-in .3s;
                    &::after {
                        content: '';
                        width: 100%;
                        background: black;
                        position: absolute;
                        height: 1px;
                        bottom: 0;
                        left: 0;
                        transition: ease-out .3s;
                    }
                }
            }
        }
    }
}
</style>