<template>
  <div
    class="modal fade"
    id="logoutModal"
    tabindex="-1"
    role="dialog"
    aria-labelledby="exampleModalLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">Ready to Leave?</h5>
          <button
            class="close"
            type="button"
            data-dismiss="modal"
            aria-label="Close"
          >
            <span aria-hidden="true">×</span>
          </button>
        </div>
        <div class="modal-body">
          Select "Logout" below if you are ready to end your current session.
        </div>
        <div class="modal-footer">
          <button class="btn btn-secondary" type="button" data-dismiss="modal">
            Cancel
          </button>
          <a class="btn btn-primary" data-dismiss="modal" @click="logout"
            >Cerrar Sesión</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import auth from '@/logic/auth'

export default {
  name: "LogoutModal",
  methods:{
    logout(){
      auth.logout();
      this.$router.push('/');
    }
  }
};
</script>

<style>
</style>