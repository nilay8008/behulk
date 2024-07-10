<nav class="bg-white border-gray-200">
  <div
    class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4"
  >
    <a href="/" class="flex items-center space-x-3 rtl:space-x-reverse">
      <img
        src="https://tsoc.dev/TSoC_Favicon.svg"
        class="h-8"
        alt="TSoC Logo"
      />
      <span class="self-center text-2xl font-semibold whitespace-nowrap hidden w-full md:block md:w-auto bg-blue-400 p-2 px-5 rounded-full bg-opacity-50"
        >TSoC Fullstack App by Nilay Patel  </span
      >
    </a>
    <button
      data-collapse-toggle="navbar-default"
      type="button"
      class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200"
      aria-controls="navbar-default"
      aria-expanded="false"
    >
      <span class="sr-only">Open main menu</span>
      <svg
        class="w-5 h-5"
        aria-hidden="true"
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 17 14"
      >
        <path
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M1 1h15M1 7h15M1 13h15"
        />
      </svg>
    </button>
    <div
      class="hidden w-full md:block md:w-auto bg-blue-400 p-3 px-5 rounded-full bg-opacity-50"
      id="navbar-default"
    >
      <ul
        class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-blue-400 rounded-lg md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0"
      >
        <li>
          <a
            href="/"
            class="block py-2 px-3 text-grey-400 rounded md:bg-transparent md:text-blue-700 md:p-0"
            aria-current="page">Home</a
          >
        </li>
        <li>
          <a
            href="/profiles"
            class="block py-2 px-3 text-grey-400 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0"
            >Profiles</a
          >
        </li>
        <li>
          <a
            href="/raw-wallet"
            class="block py-2 px-3 text-grey-400 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0"
            >Raw Wallet</a
          >
        </li>
        <li>
          <a
            href="/cloud-wallet"
            class="block py-2 px-3 text-grey-400 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0"
            >Cloud Wallet</a
          >
        </li>
        <li>
          <a
            href="/bounty"
            class="block py-2 px-3 text-grey-400 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0"
            >Bounty</a
          >
        </li>
      </ul>
    </div>
    <a
      href="https://x.com/0xScrpn"
      target="_blank"
    >
      <div
        class="mine w-15 h-15 bg-blue-500 hover:bg-blue-500"
      ></div></a
    >
  </div>
</nav>

<style>
  .mine {
    background-image: url(../../static/codecanyon.png);
    background-size: 80%;
    background-position: center;
  }
  .mine:hover {
    scale: 0.9;
    transition: all 0.4s;
    transition-timing-function: ease;
  }
</style>
