<template>
    <div class="layout-wrapper">
        <app-topbar @menubutton-click="onMenuButtonClick"/>
        <app-menu :active="sidebarActive" />
        <div :class="['layout-mask', {'layout-mask-active': sidebarActive}]" @click="onMaskClick"></div>
        <div class="layout-content">
            <router-view/>
            <app-footer />
        </div>
    </div>
</template>

<script>
import AppTopBar from '@/AppTopBar.vue';
import AppMenu from '@/AppMenu.vue';
import AppFooter from '@/AppFooter.vue';

export default {
    data() {
        return {
            sidebarActive: false
        }
    },
    watch: {
        $route() {
            this.sidebarActive = false;
        }
    },
    methods: {
        onMenuButtonClick() {
            this.sidebarActive = !this.sidebarActive;
        },
        onMaskClick(event) {
            this.sidebarActive = false;
        }
    },
    components: {
        'app-topbar': AppTopBar,
        'app-menu': AppMenu,
        'app-footer': AppFooter
    },
}
</script>

<style lang="scss">
@import './assets/styles/app.scss';
</style>
