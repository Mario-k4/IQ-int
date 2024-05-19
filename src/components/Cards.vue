<script>
</script>

<template>
  <v-container fluid class="d-flex align-center justify-center flex-column flex-md-row">
    <div class="flip">
      <div class="front rounded-xl text-center" style="background: linear-gradient(to top, #0C7AA8, #39EDF9);">
        <div class="text-h3 font-weight-bold py-8">IQ SILVER PACKAGE</div>
        <p class="text-h4 py-5 my-10 mx-5" style="border: 4px solid white;">700€</p>
        <div class="mt-10 pt-10" style="color: #F2EDBA;">Пакет 2 IQ Silver package 700 евра 2% поврат на средства(cash
          back)</div>
      </div>
      <div class="back rounded-xl text-center" style="background: linear-gradient(to top, #0C7AA8, #39EDF9);">
        <h2>Angular</h2>
        <p>Good tools make application development
          quicker and easier to maintain than if you did everything by hand..</p>
      </div>
    </div>
    <div class="flip">
      <div class="front rounded-xl text-center"
        style="height: 550px;background: linear-gradient(180deg, #F7AC3B 0%, #BE4400 100%);">
        <div class="text-h3 font-weight-bold py-8">IQ GOLD PACKAGE</div>
        <p class="text-h4 py-5 my-10 mx-5" style="border: 4px solid white;">1200€</p>
        <div class="mt-10 pt-10" style="color: #F2EDBA;">Пакет 1 IQ gold package 1.200 евра 4% поврат на средства (cash
          back)</div>
      </div>
      <div class="back rounded-xl text-center"
        style="height: 550px;background: linear-gradient(180deg, #F7AC3B 0%, #BE4400 100%);">
        <h2>Angular</h2>
        <p>Good tools make application development quicker and easier to maintain than if you did everything by hand..</p>
      </div>
    </div>
    <div class="flip">
      <div class="front rounded-xl text-center" style="background: linear-gradient(180deg, #EDA478 0%, #634536 99.48%);">
        <div class="text-h3 font-weight-bold py-8">IQ BRONZE PACKAGE</div>
        <p class="text-h4 py-5 my-10 mx-5" style="border: 4px solid white;">300€</p>
        <div class="mt-10 pt-10" style="color: #F2EDBA;">Пакет 3 IQ Bronze package 300 евра 1% поврат на средства (cash
          back)</div>
      </div>
      <div class="back rounded-xl text-center" style="background: linear-gradient(180deg, #EDA478 0%, #634536 99.48%);">
        <h2>Angular</h2>
        <p>Good tools make application development quicker and easier to maintain than if you did everything by hand..</p>
      </div>
    </div>
  </v-container>
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto+Mono');

* {
  box-sizing: border-box;
  font-weight: normal;
}

h1 {
  font-size: 2.2em;
}

/* base */
.flip {
  position: relative;
}

.flip>.front,
.flip>.back {
  display: block;
  transition-timing-function: cubic-bezier(.175, .885, .32, 1.275);
  transition-duration: .5s;
  transition-property: transform, opacity;
}

.flip>.front {
  transform: rotateY(0deg);
}

.flip>.back {
  position: absolute;
  opacity: 0;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  transform: rotateY(-180deg);
}

.flip:hover>.front {
  transform: rotateY(180deg);
}

.flip:hover>.back {
  opacity: 1;
  transform: rotateY(0deg);
}

/* custom */
.flip {
  display: inline-block;
  margin-right: 2px;
  margin-bottom: 1em;
  width: 309px;
}

.flip>.front,
.flip>.back {
  display: block;
  color: white;
  width: inherit;
  height: 495px;
  padding: 1em 2em;
  background: #313131;
  border-radius: 10px;
}

.front,
.back {
  box-shadow: 0px 4px 4px 2px rgba(0, 0, 0, 0.25);
}
</style>