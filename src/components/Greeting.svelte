<svelte:head>
  <link 
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" 
    rel="stylesheet" 
    integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" 
    crossorigin="anonymous"
  >
</svelte:head>

<script>
  // properties 
  export let name;
  export let course;
  export let description;
  export let facebookLink;
</script>

<div class="card" style="width: 18rem;">
  <div class="card-body">
    <h5 class="card-title">{name}</h5>
    <h6 class="card-subtitle mb-2 text-muted">{course}</h6>
    <p class="card-text">
      {description}
    </p>
    <a href="{facebookLink}" class="card-link" target="_blank">{name}'s Facebook account</a>
  </div>
</div>

<style>

</style>