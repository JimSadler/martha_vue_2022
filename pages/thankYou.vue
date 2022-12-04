<template>
  <div class="thank">
    <div>
      <div md="12" class="thankWhite animated zoomIn">
        <h1 class="title">
          Thank you!
        </h1>
        <p>Your form submission has been received.</p>
        <p class="homelink text-center">
          <router-link to="/" tag="button" class="button is-info">
            <span class="icon">
              <font-awesome-icon
                :icon="{ prefix: 'fas', iconName: 'arrow-left' }"
              />
            </span>
            <span>Back to Home</span>
          </router-link>
        </p>
      </div>
    </div>
  </div>
</template>
<script>
export default {}
</script>
<style scoped>
.thank {
  background-color: rgba(74, 74, 74, 0.3);
}
.thank {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 102vh;
  width: 100vw;
  margin-top: -4% !important;
}
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 48px;
  color: #35495e;
  letter-spacing: 1px;
}
.thankWhite {
  background-color: #fff;
  border-radius: 10px;
  width: 600px;
  height: 200px;
  text-align: center;
  padding-top: 3%;
}
.homelink {
  margin-top: 5%;
}
button.button {
  margin-left: 0% !important;
}
</style>
