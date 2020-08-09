<template>
    <div>
        <!-- MAIN SECTION -->
        <!-- TOP NAVBAR COMPONENT -->
        <TopNavbar/>
        <!-- END -->
        <!-- END -->
    </div>
</template>

<script>
export default {
    components: {
        TopNavbar: () => import("@/components/therapy/TopNavbar/index.vue")
    },
    data () {
        return {}
    }
}
</script>