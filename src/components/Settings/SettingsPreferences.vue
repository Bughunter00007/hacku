<template>
  <section class="box box-section">
    <box-section-item label="Boob Size" :description="`Current value: ${currentValue.boobsSize}`">
      <div class="slider-container">
        <input
          v-model="currentValue.boobsSize"
          type="range"
          class="slider"
          in="0.3"
          max="2"
          step="0.1" />
        <span class="min">0.3</span>
        <span class="max">2.0</span>
      </div>
    </box-section-item>

    <box-section-item label="Areola Size" :description="`Current value: ${currentValue.areolaSize}`">
      <div class="slider-container">
        <input
          v-model="currentValue.areolaSize"
          type="range"
          class="slider"
          in="0.3"
          max="2"
          step="0.1" />
        <span class="min">0.3</span>
        <span class="max">2.0</span>
      </div>
    </box-section-item>

    <box-section-item label="Nipple Size" :description="`Current value: ${currentValue.nippleSize}`">
      <div class="slider-container">
        <input
          v-model="currentValue.nippleSize"
          type="range"
          class="slider"
          in="0.3"
          max="2"
          step="0.1" />
        <span class="min">0.3</span>
        <span class="max">2.0</span>
      </div>
    </box-section-item>

    <box-section-item label="Vagina Size" :description="`Current value: ${currentValue.vaginaSize}`">
      <div class="slider-container">
        <input
          v-model="currentValue.vaginaSize"
          type="range"
          class="slider"
          in="0.3"
          max="1.5"
          step="0.1"></input>
        <span class="min">0.3</span>
        <span class="max">1.5</span>
      </div>
    </box-section-item>

    <box-section-item label="Pubic Hair" :description="`Current value: ${currentValue.pubicHairSize}`">
      <div class="slider-container">
        <input
          v-model="currentValue.pubicHairSize"
          type="range"
          class="slider"
          in="0"
          max="2"
          step="0.1"></input>
        <span class="min">None</span>
        <span class="max">2.0</span>
      </div>
    </box-section-item>

    <box-section-item
      label="Number of executions"
      description="The transformation can be different each time, here you can set how many times your photo will be processed. In the end you can save the one you like best.">
      <input v-model="currentValue.executions" type="number" min="1" class="input" />
    </box-section-item>

    <box-section-item v-if="false" label="Photo restoration" description="Restore the cropped photo to the original photo.">
      <select v-model="currentValue.useRestoration" class="input">
        <option :value="true">Enabled</option>
        <option :value="false">Disabled</option>
      </select>
    </box-section-item>

    <box-section-item v-if="false" label="waifu2x" description="waifu2x will try to resize your transformed photo to 1024x1024 with the least possible quality loss.">
      <select v-model="currentValue.useWaifu" class="input">
        <option :value="true">Enabled</option>
        <option :value="false">Disabled</option>
      </select>
    </box-section-item>

    <box-section-item
      v-if="false"
      label="Use Custom Mask"
      hint="(Advanced) You can edit the masks of the photo before processing.">
      <select v-model="currentValue.useCustomMask" class="input">
        <option :value="false">Disabled</option>
        <option :value="true">Enabled</option>
      </select>
    </box-section-item>
  </section>
</template>

<script>
import { VModel } from '~/mixins'

export default {
  mixins: [VModel]
}
</script>
