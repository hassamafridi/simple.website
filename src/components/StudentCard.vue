<template>
  <div>
    <div class="card">
      <div class="container">
        <h4><b>{{student.name}}</b></h4>
        <p>{{student.email}}</p>
        <p>{{student.phone}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props: ['student']
};
</script>

<style>
.card {
    float: left;
  width: 350px;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container {
  padding: 2px 16px;
}
</style>




