<script>
  export default {
    data() {
	return {
		name: 'чебупели',
    attr: 'che.jpg',
    text: 'page',
		href: 'page.html',
	}
}
  }
</script>

<template>
  <div>
		<h1> vue exercises :)</h1>
	</div>
  <br>
  <img :src="attr">
  <div> <p> {{ name }}</p>
    <p>купи меня пожалуйста <a href="page.html">тут</a></p>
  </div>
</template>

<style >
header {
  line-height: 1.5;
}
p {
  line-height: 2;
  font-size: medium;
  letter-spacing: 1.2px;
  font-family: 'Lucida Sans Unicode','Lucida Grande','sans-serif';
  color: rgb(0, 0, 0);
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