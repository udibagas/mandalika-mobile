<template>
  <div>
    <strong>PRAKIRAAN CUACA</strong>
    <br />
    <br />
    <f7-row no-gap>
      <f7-col :span="6" class="text-center">
        <div style="font-size:16px">Malam</div>

        <div style="font-size:37px">
          <f7-icon f7="cloud_drizzle"></f7-icon>
        </div>

        <strong>
          10 &deg;F
          <br />10%
        </strong>
        <br />
        <small>Gerimis</small>
      </f7-col>
      <f7-col :span="6" class="text-center">
        <div style="font-size:16px">Pagi</div>

        <div style="font-size:37px">
          <f7-icon f7="cloud_heavyrain"></f7-icon>
        </div>

        <strong>
          10 &deg;F
          <br />10%
        </strong>
        <br />
        <small>Hujan</small>
      </f7-col>
      <f7-col :span="6" class="text-center">
        <div style="font-size:16px">Siang</div>

        <div style="font-size:37px">
          <f7-icon f7="sun_max"></f7-icon>
        </div>

        <strong>
          10 &deg;F
          <br />10%
        </strong>
        <br />
        <small>Cerah</small>
      </f7-col>
      <f7-col :span="6" class="text-center">
        <div style="font-size:16px">Sore</div>

        <div style="font-size:37px">
          <f7-icon f7="cloud"></f7-icon>
        </div>

        <strong>
          10 &deg;F
          <br />10%
        </strong>
        <br />
        <small>Berawan</small>
      </f7-col>
    </f7-row>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.text-center {
  text-align: center;
}
</style>
