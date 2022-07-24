<template>
    <NavbarComponent/>
    <div class="d-flex">
        <div class="col-4">
            <EntrylistComponent/>
        </div>
        <div class="col">
            <router-view/>
        </div>
    </div>
</template>

<script>
import { defineAsyncComponent } from "vue";

export default {
    components:{
    NavbarComponent: defineAsyncComponent(() => import("../components/NavbarComponent")),
    EntrylistComponent: defineAsyncComponent(() => import("../components/EntrylistComponent")),
}
}
</script>
