<template>
  <div class="container-fluid">
    <section class="row">
      <div class="col-12 text-center">
        <button data-bs-toggle="modal" data-bs-target="#modalOne" class="btn btn-outline-info">
          Open First Modal
        </button>
        <button data-bs-toggle="modal" data-bs-target="#modalTwo" class="btn btn-outline-info">
          Open Second Modal
        </button>
        <button data-bs-toggle="modal" data-bs-target="#modalThree" class="btn btn-outline-info">
          Open Second Modal
        </button>
      </div>
    </section>
  </div>

  <ModalComponent :modalId="'modalOne'">
    <template #modalTitle>
      <b>Modal One</b>
    </template>

    <template #modalBody>
      Sup doggies
    </template>
  </ModalComponent>

  <ModalComponent :modalId="'modalTwo'" :modalSize="'modal-sm'" :showFooter="true">
    <template #modalTitle>
      <i>Modal Two</i>
    </template>

    <template #modalBody>
      <CatForm />
    </template>
  </ModalComponent>

  <ModalComponent :modalId="'modalThree'" :modalSize="'modal-fullscreen'">
    <template #modalTitle>
      Modal Three
    </template>

  </ModalComponent>
</template>

<script>
import CatForm from '../components/CatForm.vue';
import ModalComponent from '../components/ModalComponent.vue';

export default {
  setup() {
    return {};
  },
  components: { ModalComponent, CatForm }
}
</script>

<style scoped lang="scss"></style>
