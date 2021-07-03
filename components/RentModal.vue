<template>
  <div>
    <b-button id="show-btn" @click="showModal">Rent</b-button>
  

    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
        <div class="calender-container">
            <div class="text-container">
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Praesentium fuga mollitia, eos architecto reprehenderit officia placeat atque explicabo animi ratione odit nobis! Expedita deleniti id excepturi qui minus eaque, cupiditate veniam voluptas ipsum reiciendis blanditiis ipsam exercitationem. Numquam, maxime inventore?</p>
            </div>
        </div>
    </b-modal>
  </div>
</template>

<script>
  export default {
    methods: {
      showModal() {
        this.$refs['my-modal'].show()
      },
      hideModal() {
        this.$refs['my-modal'].hide()
      },
      toggleModal() {
        // We pass the ID of the button that we want to return focus to
        // when the modal has hidden
        this.$refs['my-modal'].toggle('#toggle-btn')
      }
    }
  }
</script>