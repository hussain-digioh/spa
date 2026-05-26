<template>
  <div class="digioh-widget-wrapper">
    <div
      class="digioh_universal_smart_tag"
      id="digioh-form"
      style="text-align: center;"
    >
      <div
        class="box_loading_placeholder"
        style="position: relative; text-align: center; border-style: none; border-width: 0px; background-color: #fff; height: 750px; width: 100%;"
      >
        <div
          class="box_loading_placeholder_overlay"
          style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: rgba(255,255,255,0.25);"
        ></div>
        <div style="position: relative; top: 50%; transform: translateY(-50%);">
          <img
            class="box_loading_placeholder_image"
            src="https://www.lightboxcdn.com/static/Digioh_Loading_Spinner_Black.gif"
            style="margin: 0 auto; max-height: 100%; max-width: 100%; width: 125px;"
            alt="Loading..."
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.digioh-widget-wrapper {
  width: 100%;
  background: var(--dg-white);
}
</style>
