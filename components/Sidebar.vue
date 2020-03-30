<template>
    <ul class="navbar-nav bg-gradient-primary sidebar sidebar-dark accordion" id="accordionSidebar">
        <a class="sidebar-brand d-flex align-items-center justify-content-center" href="home">
            <!-- <div class="sidebar-brand-icon rotate-n-15">
                <i class="fas fa-laugh-wink"></i>
            </div> -->
            <div class="sidebar-brand-text mx-3">EVERMOS</div>
        </a>
        <div class="sidebar-heading">
            Admin
        </div>
        <hr class="sidebar-divider my-0">
        <li class="nav-item active">
            <a class="nav-link" href="dashboard">
                <i class="fas fa-fw fa-tachometer-alt"></i>
                <span>Dashboard</span>
            </a>
        </li>
        <hr class="sidebar-divider">
        <div class="sidebar-heading">
            Employee
        </div>
        
        <li class="nav-item">
            <a class="nav-link collapsed" href="questionnaire">
                <i class="fas fa-fw fa-laptop"></i>
                <span>Questionnaire</span>
            </a>
        </li>
        <li class="nav-item">
            <a class="nav-link collapsed" href="profile" >
                <i class="fas fa-fw fa-user"></i>
                <!-- <img src="abstract-user-flat-4.svg" /> -->
                <span>Profile</span>
            </a>
        </li>
        <li class="nav-item">
            <a class="nav-link collapsed" href="courses" >
                <i class="fas fa-fw fa-sticky-note"></i>
                <span>Courses</span>
            </a>
        </li>
    </ul>
</template>

<script>
export default {
    
}
</script>