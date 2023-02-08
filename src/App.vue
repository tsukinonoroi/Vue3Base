<script>
  export default {
    data() {
	return {
		name: 'Edem',
		surn: 'Seytumerov',
	}
}
  }
</script>

<template>
  <div>
		<h1> I'm doing vue project </h1>
	</div>
  <br>
  <div> <p> Hello, my name is {{ name }} {{ surn }}</p>
  </div>
</template>

<style >
header {
  line-height: 1.5;
}
p {
  line-height: 3;
  font-size: large;
  letter-spacing: 3.5px;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', sans-serif;
  color: rgb(154, 155, 255);
}
.logo {
  display: block;
  margin: 0 auto 2rem;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }
  .logo {
    margin: 0 2rem 0 0;
  }
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
