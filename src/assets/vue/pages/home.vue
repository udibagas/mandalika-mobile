<template>
  <f7-page style="background-color:#ddd">
    <f7-navbar no-shadow bg-color="red">
      <div class="title">MANDALIKA WIND</div>
    </f7-navbar>

    <!-- KECEPATAN ANGIN -->
    <f7-row no-gap>
      <f7-col>
        <f7-card style="padding:10px">
          <Kecepatan :height="100" el="kecepatan-100" />
        </f7-card>
      </f7-col>
      <f7-col>
        <f7-card style="padding:10px">
          <Kecepatan :height="70" el="kecepatan-70" />
        </f7-card>
      </f7-col>
    </f7-row>

    <f7-row no-gap>
      <f7-col>
        <f7-card style="padding:10px">
          <Kecepatan :height="40" el="kecepatan-40" />
        </f7-card>
      </f7-col>
      <f7-col>
        <f7-card style="padding:10px">
          <Kecepatan :height="10" el="kecepatan-10" />
        </f7-card>
      </f7-col>
    </f7-row>

    <!-- SUHU -->
    <f7-card style="padding:10px">
      <Suhu :height="100" el="suhu-100" />
    </f7-card>
    <f7-card style="padding:10px">
      <Suhu :height="10" el="suhu-10" />
    </f7-card>
    <f7-card style="padding:10px">
      <Suhu :height="2" el="suhu-2" />
    </f7-card>

    <!-- TEKANAN -->
    <f7-card style="padding:10px">
      <Tekanan :height="100" el="tekanan-100" />
    </f7-card>
    <f7-card style="padding:10px">
      <Tekanan :height="10" el="tekanan-10" />
    </f7-card>
    <f7-card style="padding:10px">
      <Tekanan :height="2" el="tekanan-2" />
    </f7-card>

    <!-- HUJAN -->
    <f7-row no-gap>
      <f7-col>
        <f7-card style="padding:10px">
          <CurahHujan :height="2" el="curah-hujan" />
        </f7-card>
      </f7-col>
      <f7-col>
        <f7-card style="padding:10px">
          <HujanSaatIni :height="2" el="hujan-saat-ini" />
        </f7-card>
      </f7-col>
    </f7-row>

    <!-- HUJAN -->
    <f7-row no-gap>
      <f7-col>
        <f7-card style="padding:10px">
          <Kelembaban el="kelembaban" />
        </f7-card>
      </f7-col>
      <f7-col>
        <f7-card style="padding:10px">
          <Penguapan el="penguapan" />
        </f7-card>
      </f7-col>
    </f7-row>

    <!-- MATAHARI -->
    <f7-row no-gap>
      <f7-col>
        <f7-card style="padding:10px">
          <Uv el="uv" />
        </f7-card>
      </f7-col>
      <f7-col>
        <f7-card style="padding:10px">
          <RadiasiMatahari el="radiasi-matahari" />
        </f7-card>
      </f7-col>
    </f7-row>

    <f7-card style="padding:10px">
      <TerbitTerbenam />
    </f7-card>

    <!-- CUACA -->
    <f7-card style="padding:10px">
      <PrakiraanCuaca />
    </f7-card>
  </f7-page>
</template>

<script>
import Suhu from "../components/udara/Suhu";
import Tekanan from "../components/udara/Tekanan";
import CurahHujan from "../components/udara/CurahHujan";
import Kecepatan from "../components/angin/Kecepatan";
import HujanSaatIni from "../components/HujanSaatIni";
import Penguapan from "../components/udara/Penguapan";
import Kelembaban from "../components/udara/Kelembaban";
import Uv from "../components/Uv";
import RadiasiMatahari from "../components/RadiasiMatahari";
import PrakiraanCuaca from "../components/PrakiraanCuaca";
import TerbitTerbenam from "../components/TerbitTerbenam";

export default {
  components: {
    Suhu,
    Kecepatan,
    Tekanan,
    CurahHujan,
    HujanSaatIni,
    Penguapan,
    Kelembaban,
    Uv,
    RadiasiMatahari,
    PrakiraanCuaca,
    TerbitTerbenam
  }
};
</script>
