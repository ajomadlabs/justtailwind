<template>
    <div>
        <!-- MAIN SECTION -->
        <!-- TOP NAVBAR COMPONENT -->
        <TopNavbar/>
        <!-- END -->
        <!-- PROFILE COMPONENT -->
        <Profile
            class="xs:mt-24 lg:mt-38"
        />
        <!-- END -->
        <!-- END -->
    </div>
</template>

<script>
export default {
    components: {
        TopNavbar: () => import("@/components/01/TopNavbar/index.vue"),
        Profile: () => import("@/components/01/Profile/index.vue")
    },
    data () {
        return {}
    }
}
</script>