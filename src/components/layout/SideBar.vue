<template>
  <div class="d-flex content h-100">
    <div class="d-flex">
      <input class="icon-show" type="checkbox" id="show" checked>
      <div class="sidebar fs-14">
        <div class="logo-sidebar">
          <img class="w-100" src="../../assets/images/logo.png" alt>
        </div>
        <a class="list-staff d-flex justify-content-between" href="#" @click="openStaff">
          <div class="d-flex align-items-center">
            <div class="icon-user">
              <img class="w-100" src="../../assets/images/icons/user.png">
            </div>
            <p class="mb-0 ms-2">Nhân viên</p>
          </div>
          <label class="icon" for="show-detail-staff">
            <img class="w-100" src="../../assets/images/icons/right-arrow.png">
          </label>
        </a>
        <input type="checkbox" class="d-none" id="show-detail-staff" checked>
        <div class="staff-detail">
          <a class="staff-item" href="#" @click="openListStaff">Danh sách nhân viên</a>
          <a class="staff-item" href="#" @click="openAddStaff">Thêm nhân viên</a>
        </div>

        <a class="list-staff d-flex justify-content-between" href="#" @click="openCustomer">
          <div class="d-flex align-items-center">
            <div class="icon-user">
              <img class="w-100" src="../../assets/images/icons/user.png">
            </div>
            <p class="mb-0 ms-2">Khách hàng</p>
          </div>
          <label id="abc" class="icon" for="show-detail-custumer">
            <img class="w-100" src="../../assets/images/icons/right-arrow.png">
          </label>
        </a>
        <input type="checkbox" class="d-none" id="show-detail-custumer" checked>
        <div class="custumer-detail">
          <a class="custumer-item" href="#" @click="openListCustomer">Danh sách khách hàng</a>
          <a class="custumer-item" href="#" @click="openAddCustomer">Thêm khách hàng</a>
        </div>
      </div>
    </div>

    <div class="main-content">
      <div class="heading d-flex justify-content-between align-items-center">
        <label class="btn-toogle" for="show">
          <img class="w-100" src="../../assets/images/icons/menu.png">
        </label>
        <a class="avatar me-3" href="#">
          <img class="w-100" src="../../assets/images/img-user.png">
        </a>
      </div>
      <router-view />
      <div class="d-flex justify-content-between license fs-12 text-secondary">
        <p class="mb-0"><a class="text-decoration-none" href="#"> CoreUI© </a> 2020 creativeLabs.</p>
        <p class="mb-0">
          Powered by
          <a class="text-decoration-none" href="#">
            Bootstrap

          </a>
          &
          <a class="text-decoration-none" href="#">
            VueJS
          </a>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import router from "@/router";

export default {
  name: "SideBar",
  methods: {
    openStaff() {
      router.push('/home/staff/')
    },
    openListStaff() {
      router.push('/home/list-staff/')
    },
    openAddStaff() {
      router.push('/home/add-staff/')
    },
    openCustomer() {
      router.push('/home/customer/')
    },
    openListCustomer() {
      router.push('/home/list-customer/')
    },
    openAddCustomer() {
      router.push('/home/add-customer/')
    }
  }
}
</script>
<style>
@import "../../assets/SCSS/_side-bar.scss";
</style>