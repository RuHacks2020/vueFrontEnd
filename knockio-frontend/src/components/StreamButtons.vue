<template>
    <div :id="id">
        <button>{{buttonName}}</button>
    </div>
</template>

<script>
export default {
    name: 'StreamButtons',
    id: 'grab-photo',
    props: ['buttonName'],
}
</script>