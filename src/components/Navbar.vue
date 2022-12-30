<template>
    <div>
        <ul class="nav justify-content-center">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Home</a>
            </li>
            <b-nav-item-dropdown text="Category" right>
                <b-dropdown-item href="#">Men's Clothing</b-dropdown-item>
                <b-dropdown-item href="#">Women's Clothing</b-dropdown-item>
              </b-nav-item-dropdown>
            <li class="nav-item">
              <a class="nav-link active">About</a>
            </li>
          </ul>
    </div>
</template>
<script>
export default {
    name:'Navbar'
}
</script>
<style>
    
</style>