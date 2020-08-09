<template>
    <div>
        <!-- MAIN SECTION -->
        <!-- TOP NAVBAR COMPONENT -->
        <TopNavbar/>
        <!-- END -->
        <!-- PROFILE COMPONENT -->
        <Profile
            class="mt-38"
        />
        <!-- END -->
        <!-- END -->
    </div>
</template>

<script>
export default {
    components: {
        TopNavbar: () => import("@/components/therapy/TopNavbar/index.vue"),
        Profile: () => import("@/components/therapy/Profile/index.vue")
    },
    data () {
        return {}
    }
}
</script>