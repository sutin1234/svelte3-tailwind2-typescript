<script lang="ts">
  import { link } from "svelte-routing";

  // core components
  const github = "../assets/img/github.svg";
  const google = "../assets/img/google.svg";
  export const location = '';
</script>

<div class="container h-full px-4 mx-auto">
  <div class="flex items-center content-center justify-center h-full">
    <div class="w-full px-4 lg:w-4/12">
      <div
        class="relative flex flex-col w-full min-w-0 mb-6 break-words bg-gray-300 border-0 rounded-lg shadow-lg"
      >
        <div class="px-6 py-6 mb-0 rounded-t">
          <div class="mb-3 text-center">
            <h6 class="text-sm font-bold text-gray-600">
              Sign in with
            </h6>
          </div>
          <div class="text-center btn-wrapper">
            <button
              class="inline-flex items-center px-4 py-2 mb-1 mr-2 text-xs font-normal font-bold text-gray-800 uppercase transition-all duration-150 ease-linear bg-white rounded shadow outline-none active:bg-gray-100 focus:outline-none hover:shadow-md"
              type="button"
            >
              <img alt="..." class="w-5 mr-1" src="{github}" />
              Github
            </button>
            <button
              class="inline-flex items-center px-4 py-2 mb-1 mr-1 text-xs font-normal font-bold text-gray-800 uppercase transition-all duration-150 ease-linear bg-white rounded shadow outline-none active:bg-gray-100 focus:outline-none hover:shadow-md"
              type="button"
            >
              <img alt="..." class="w-5 mr-1" src="{google}" />
              Google
            </button>
          </div>
          <hr class="mt-6 border-gray-400 border-b-1" />
        </div>
        <div class="flex-auto px-4 py-10 pt-0 lg:px-10">
          <div class="mb-3 font-bold text-center text-gray-500">
            <small>Or sign in with credentials</small>
          </div>
          <form>
            <div class="relative w-full mb-3">
              <label
                class="block mb-2 text-xs font-bold text-gray-700 uppercase"
                for="grid-email"
              >
                Email
              </label>
              <input
                id="grid-email"
                type="email"
                class="w-full px-3 py-3 text-sm text-gray-700 placeholder-gray-400 transition-all duration-150 ease-linear bg-white rounded shadow focus:outline-none focus:shadow-outline"
                placeholder="Email"
              />
            </div>

            <div class="relative w-full mb-3">
              <label
                class="block mb-2 text-xs font-bold text-gray-700 uppercase"
                for="grid-password"
              >
                Password
              </label>
              <input
                id="grid-password"
                type="password"
                class="w-full px-3 py-3 text-sm text-gray-700 placeholder-gray-400 transition-all duration-150 ease-linear bg-white rounded shadow focus:outline-none focus:shadow-outline"
                placeholder="Password"
              />
            </div>
            <div>
              <label class="inline-flex items-center cursor-pointer">
                <input
                  id="customCheckLogin"
                  type="checkbox"
                  class="w-5 h-5 ml-1 text-gray-800 transition-all duration-150 ease-linear form-checkbox"
                />
                <span class="ml-2 text-sm font-semibold text-gray-700">
                  Remember me
                </span>
              </label>
            </div>

            <div class="mt-6 text-center">
              <button
                class="w-full px-6 py-3 mb-1 mr-1 text-sm font-bold text-white uppercase transition-all duration-150 ease-linear bg-gray-900 rounded shadow outline-none active:bg-gray-700 hover:shadow-lg focus:outline-none"
                type="button"
              >
                Sign In
              </button>
            </div>
          </form>
        </div>
      </div>
      <div class="relative flex flex-wrap mt-6">
        <div class="w-1/2">
          <a href="#pablo" on:click={(e) => e.preventDefault()} class="text-gray-300">
            <small>Forgot password?</small>
          </a>
        </div>
        <div class="w-1/2 text-right">
          <a use:link href="/auth/register" class="text-gray-300">
            <small>Create new account</small>
          </a>
        </div>
      </div>
    </div>
  </div>
</div>
