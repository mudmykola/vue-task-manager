<template>
  <div></div>
</template>

<script>
export default {
data: () => ({
    selectItem: 3,
    drawer: null,
    items: [
        {
            icon: 'fas fa-tv'
        },
         {
            icon: 'far fa-building'
        },
         {
            icon: 'far fa-compass'
        },
        {
            icon: 'far fa-folder-open'
        },
        {
            icon: 'far fa-clock'
        },
        {
            icon: 'far fa-bell'
        },
        {
            icon: 'far fa-adress-book'
        },
    ],
})
}
</script>

<style>
.border{
    margin: 0 15px;
    background: #a9ddd8;
    border-radius: 50%;
    text-decoration: none;
}
</style>