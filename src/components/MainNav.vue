<template>
    <div class="header">
        <!-- Navbar -->
        <div class="navbar navbar-default mega-menu" role="navigation">
            <div class="container">
                <!-- Brand and toggle get grouped for better mobile display -->
                <div class="navbar-header">
                    <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-responsive-collapse">
                        <span class="sr-only">Toggle navigation</span>
                        <span class="fa fa-bars"></span>
                    </button>
                    <a class="navbar-brand" href="index.html">
                        <img id="logo-header" src="assets/img/logo1-default.png" alt="Logo">
                    </a>
                </div>

                <!-- Collect the nav links, forms, and other content for toggling -->
                <div class="collapse navbar-collapse navbar-responsive-collapse">
                    <ul class="nav navbar-nav">
                        <!-- Home -->
                        <li class="dropdown active">
                            <a href="javascript:void(0);" class="dropdown-toggle" data-toggle="dropdown">
                                Home
                            </a>
                            <ul class="dropdown-menu">
                                <li class="active"><a href="index.html">Option 1: Default Page</a></li>

                                <!-- One Page -->
                                <li class="dropdown-submenu">
                                    <a href="javascript:void(0);">Option 2: One Page</a>
                                    <ul class="dropdown-menu">
                                        <li><a target="_blank" href="One-Page/index.html">- One Page Template</a></li>
                                        <li><a target="_blank" href="One-Page/dark-page-example.html">- One Page Dark Theme</a></li>
                                    </ul>
                                </li>
                                <!-- End One Page -->

                                <!-- Shop UI Page -->
                                <li class="dropdown-submenu">
                                    <a href="javascript:void(0);">Option 3: Shop UI</a>
                                    <ul class="dropdown-menu">
                                        <li><a target="_blank" href="Shop-UI/index.html">- Home Page</a></li>
                                        <li><a target="_blank" href="Shop-UI/shop-ui-inner.html">- Product Page</a></li>
                                        <li><a target="_blank" href="Shop-UI/shop-ui-filter-grid.html">- Filter Grid Page</a></li>
                                        <li><a target="_blank" href="Shop-UI/shop-ui-filter-list.html">- Filter List Page</a></li>
                                        <li><a target="_blank" href="Shop-UI/shop-ui-add-to-cart.html">- Checkout Page</a></li>
                                        <li><a target="_blank" href="Shop-UI/shop-ui-login.html">- Login Page</a></li>
                                        <li><a target="_blank" href="Shop-UI/shop-ui-register.html">- Registration Page</a></li>
                                    </ul>
                                </li>
                                <!-- End Shop UI -->

                                <li><a href="page_home8.html">Option 4: Home Discover</a></li>
                                <li><a href="page_home9.html">Option 5: Home Creative</a></li>
                                <li><a href="page_home10.html">Option 6: Home Inspire</a></li>
                                <li><a href="page_home11.html">Option 7: Home Desire</a></li>
                                <li><a href="page_jobs.html">Option 8: Home Jobs</a></li>
                                <li><a href="page_home3.html">Option 9: Amazing Content</a></li>
                                <li><a href="page_home6.html">Option 10: Home Magazine</a></li>
                                <li><a href="page_home4.html">Option 11: Home Sidebar</a></li>
                                <li><a href="page_home7.html">Option 12: Home Portfolio</a></li>
                                <li><a href="page_home1.html">Option 13: Home Default v1</a></li>
                                <li><a href="page_home2.html">Option 14: Home Default v2</a></li>
                                <li><a href="page_home5.html">Option 15: Home Default v3</a></li>

                                <!-- Misc Pages -->
                                <li class="dropdown-submenu">
                                    <a href="javascript:void(0);">Options: Misc Pages</a>
                                    <ul class="dropdown-menu">
                                        <li><a href="page_misc_blank.html">- Blank page</a></li>
                                        <li><a href="page_misc_boxed.html">- Boxed Page</a></li>
                                        <li><a href="page_misc_boxed_img.html">- Boxed Image Page</a></li>
                                        <li><a href="page_misc_boxed_fixed_header.html">- Boxed Fixed Menu</a></li>
                                        <li><a href="page_misc_fixed_header.html">- Fixed Menu</a></li>
                                        <li><a href="page_misc_dark.html">- Dark Page</a></li>
                                        <li><a href="page_misc_dark_boxed.html">- Dark Boxed Page</a></li>
                                        <li><a href="page_misc_dark_other_color.html">- Dark Page With Different Theme Color</a></li>
                                    </ul>
                                </li>
                                <!-- End Misc Pages -->
                            </ul>
                        </li>
                        <!-- End Home -->

                        <!-- Contacts -->
                        <li class="dropdown">
                            <a href="javascript:void(0);" class="dropdown-toggle" data-toggle="dropdown">
                                Contacts
                            </a>
                            <ul class="dropdown-menu">
                                <li><a href="page_contact1.html">Contacts Default</a></li>
                                <li><a href="page_contact_advanced.php">Contacts Advanced</a></li>
                                <li><a href="page_contact2.html">Contacts Option 1</a></li>
                                <li><a href="page_contact3.html">Contacts Option 2</a></li>
                                <li><a href="page_contact4.html">Contacts Option 3</a></li>
                            </ul>
                        </li>
                        <!-- End Contacts -->

                    </ul>
                </div>
                <!--/navbar-collapse-->
            </div>
        </div>
        <!-- End Navbar -->
    </div>
</template>

<script>
    export default {
        name: 'MainNav',
        //props: ['displayName', 'pictureUrl'],
        //components: { SidebarMenu },
        mounted: function () {
        }
    }

</script>

<style>
    .header { margin-top: 10px; }
    .navbar-toggle { border: solid 3px red; background-color: orangered; border-radius: 5px;}
</style>