<template>
    <input type="number" min=minInput max=maxInput/>
</template>


<script>
    defineProps({
        "minInput":Number,
        "maxInput":Number
    })

</script>