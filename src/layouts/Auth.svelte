<script lang="ts">
  import { Router, Route } from "svelte-routing";

  // components for this layout
  import AuthNavbar from "components/Navbars/AuthNavbar.svelte";
  import FooterSmall from "components/Footers/FooterSmall.svelte";

  // pages for this layout
  import Login from "views/auth/Login.svelte";
  import Register from "views/auth/Register.svelte";

  const registerBg2 = "../assets/img/register_bg_2.png";
  export const location = '';
  export const auth = "";
</script>

<div>
  <AuthNavbar />
  <main>
    <section class="relative w-full h-full min-h-screen py-40">
      <div
        class="absolute top-0 w-full h-full bg-gray-900 bg-no-repeat bg-full"
        style="background-image: url({registerBg2});"
      ></div>
      <Router url="auth">
        <Route path="login" component="{Login}" />
        <Route path="register" component="{Register}" />
      </Router>
      <FooterSmall absolute="true" />
    </section>
  </main>
</div>
