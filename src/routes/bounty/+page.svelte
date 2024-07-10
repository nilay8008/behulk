<script lang="ts">
  export let form;
  let last = 0;
</script>

<div class="bounty-page">
  <div
    class=" pt-6 w-screen max-w-screen-lg p-12 mx-auto rounded-lg shadow-xl dark:bg-white/10 bg-white/30 ring-1 ring-gray-900/5 backdrop-blur-lg"
  >
    <form method="POST" action="?/deploy">
      <h1 class="font-bold text-lg">Deploy A Bounty</h1>
      <div class="flex flex-wrap -mx-3 mb-2 w-12/12 justify-evenly">
        <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-city"
          >
            Bounty
          </label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="bounty"
            type="number"
            placeholder="Enter Bounty Amount"
            name="bounty"
            required
          />
        </div>
        <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-city"
          >
            Enter the number whose square root is on bounty
          </label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="square"
            type="number"
            placeholder="Enter Number"
            name="square"
            required
          />
        </div>
        <br />
        <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-city"
          >
            Email
          </label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-2 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="email"
            type="text"
            placeholder="Enter email"
            name="email"
            required
          />
        </div>
        <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-city"
          >
            Password
          </label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="password"
            type="text"
            placeholder="Enter password"
            name="password"
            required
          />
        </div>
        <!-- <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
<label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-state">
  Email
  </label>
  </div> -->
        <button
          type="submit"
          class="bg-yellow-500 hover:bg-blue-700 text-white font-bold mt-5 ml-2 px-2 rounded"
          on:click={() => {
            last = 0;
          }}
        >
          Deploy Bounty
        </button>
      </div>
    </form>
    {#if last == 0}
      {#if form?.success}
        <!-- this message is ephemeral; it exists because the page was rendered in
response to a form submission. it will vanish if the user reloads -->
        <p class="pt-2">
          Bounty was deployed successfully

          <a
            href="http://whatsonchain.com/tx/{form?.tx}"
            class="text-blue-500"
            target="_blank"
          >
            transaction link</a
          >
        </p>
      {/if}
    {/if}
  </div>
  <div
    class="mt-4 pt-10 w-screen max-w-screen-lg p-12 mx-auto rounded-lg shadow-xl dark:bg-white/10 bg-white/30 ring-1 ring-gray-900/5 backdrop-blur-lg"
  >
    <form method="POST" action="?/unlock">
      <h1 class="font-bold text-lg">Unlock This Bounty</h1>
      <div class="flex flex-wrap -mx-3 mb-2 w-12/12 justify-evenly">
        <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-city"
          >
            Root
          </label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="root"
            type="number"
            placeholder="Enter Root answer"
            name="root"
            required
          />
        </div>
        <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-city"
          >
            Email
          </label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-2 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="email"
            type="text"
            placeholder="Enter email"
            name="email"
            required
          />
        </div>
        <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-city"
          >
            Password
          </label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="password"
            type="text"
            placeholder="Enter password"
            name="password"
            required
          />
        </div>
        <button
          type="submit"
          class="bg-yellow-500 hover:bg-blue-700 text-white font-bold mt-5 ml-2 px-2 rounded"
          on:click={() => {
            last = 1;
          }}
        >
          Unlock Bounty
        </button>
      </div>
    </form>
    {#if last == 1}
      {#if form?.success}
        <!-- this message is ephemeral; it exists because the page was rendered in
response to a form submission. it will vanish if the user reloads -->
        <p class="pt-2">
          Bounty was unlocked successfully
          <a
            href="http://whatsonchain.com/tx/{form?.tx}"
            target="_blank"
            class="text-blue-500">transaction link</a
          >
        </p>
      {/if}
    {/if}
  </div>

  <div class="h-32"></div>
</div>

<style>
</style>
