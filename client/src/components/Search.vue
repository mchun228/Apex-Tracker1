<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  data() {
    return {
      platform: '' as string, // Initialize with the appropriate data type
      gamertag: '' as string,
    };
  }
});
</script>
<template>
    <section class = "search">
        <h1>Tracker Player Stats</h1>
        <form v-on:submit.prevent="onSubmit">
            <div class = "form-group">
                <label for="platform">Platform</label>
                <select name="platform" id = "platform" v-model="platform">
                    <option value="psn">Playstation</option>
                    <option value="xbl">Xbox</option>
                    <option value="Origin">Origin</option>
                </select>
            </div>
            <div class="form-group"><a/div>
                <label for="gamertag">Gamertag</label>
                <input type="text" name="gamertag" id="gamertag" v-model="gamertag">
        </form>
    </section>
</template>