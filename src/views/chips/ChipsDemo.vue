<template>
    <div>
        <div class="content-section introduction">
            <div class="feature-intro">
                <h1>Chips</h1>
                <p>Chips is used to enter multiple values on an input field.</p>
            </div>
        </div>

        <div class="content-section implementation">
            <h3 class="first">Basic</h3>
            <p-chips v-model="value1" />

            <h3>Template</h3>
            <p-chips v-model="value2">
                <template slot-scope="{value}">
                    <div>
                        <span>{{value}} - (active) </span>
                        <i class="pi pi-user-plus" style="font-size: 14px"></i>
                    </div>
                </template>
            </p-chips>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            value1: null,
            value2: null
        }
    }
}
</script>

<style>
.p-chips .p-inputtext {
    width: 100%;
}
</style>
