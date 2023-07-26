<template>
  <div class="flex h-full bg-gray-200">
    <Sidebar />
    <div class="flex-1 flex flex-col overflow-x-hidden">
      <Navbar />
      <main class="flex-1 overflow-x-hidden bg-[#FFFFFF]">
        <div class="px-8 py-4 h-screen">
          <div>
            <p class="text-gray-500">
              Konfugurasi /
              <span class="text-gray-800">Data Daftar Truk</span>
            </p>
            <p class="text-2xl font-semibold mt-3">Data Daftar Truk</p>
            <p class="text-gray-500">Informasi List Daftar truk</p>
          </div>

          <div
            class="flex flex-wrap items-center justify-items-center justify-between"
          >
            <div
              class="flex items-center text-lg mt-10 mb-6 md:mb-8 bg-gray-200 px-3 w-96 rounded-lg"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="h-6 w-6 text-gray-700"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z"
                />
              </svg>

              <input
                type="text"
                id="username"
                class="form-controll text-base bg-gray-200 text-gray-600 rounded-lg font-thin text pl-3 py-3 focus:outline-none w-full"
                placeholder="Cari truk"
              />
            </div>

            <button
              type="button"
              class="h-12 bg-primary-9 mb-3 text-white font-semibold rounded-lg w-44 flex justify-center items-center"
            >
              <p>Tambah Truk</p>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-6 h-6"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M12 6v12m6-6H6"
                />
              </svg>
            </button>
          </div>

          <div class="relative overflow-x-auto">
            <table
              class="w-full text-sm text-left text-gray-500 dark:text-gray-400"
            >
              <thead
                class="text-gray-500 dark:bg-gray-700 dark:text-gray-400 border-b"
              >
                <tr>
                  <th scope="col" class="px-6 py-3">
                    <div class="flex items-center justify-between">
                      ID Truk
                      <a href="#">
                        <img
                          class="h-2 md:h-5"
                          src="../../../public/icon/Table-up-and-down-arrow.png"
                          alt="Image up down arrow"
                        />
                      </a>
                    </div>
                  </th>

                  <th scope="col" class="px-6 py-3">
                    <div class="flex items-center justify-between">
                      Jenis Kendaraan
                      <a href="#">
                        <img
                          class="h-5"
                          src="../../../public/icon/Table-up-and-down-arrow.png"
                          alt="Image up down arrow"
                        />
                      </a>
                    </div>
                  </th>

                  <th scope="col" class="px-6 py-3">
                    <div class="flex items-center justify-between">
                      Merek
                      <a href="#">
                        <img
                          class="h-5"
                          src="../../../public/icon/Table-up-and-down-arrow.png"
                          alt="Image up down arrow"
                        />
                      </a>
                    </div>
                  </th>

                  <th scope="col" class="px-6 py-3">
                    <div class="flex items-center justify-between">
                      Tipe Kendaraan
                      <a href="#">
                        <img
                          class="h-5"
                          src="../../../public/icon/Table-up-and-down-arrow.png"
                          alt="Image up down arrow"
                        />
                      </a>
                    </div>
                  </th>

                  <th scope="col" class="px-6 py-3">
                    <div class="flex items-center justify-between">
                      Volume
                      <a href="#">
                        <img
                          class="h-5"
                          src="../../../public/icon/Table-up-and-down-arrow.png"
                          alt="Image up down arrow"
                        />
                      </a>
                    </div>
                  </th>

                  <th scope="col" class="px-6 py-3">
                    <div class="flex items-center justify-between">
                      Kapasitas
                      <a href="#">
                        <img
                          class="h-5"
                          src="../../../public/icon/Table-up-and-down-arrow.png"
                          alt="Image up down arrow"
                        />
                      </a>
                    </div>
                  </th>

                  <th scope="col" class="px-6 py-3">
                    <div class="flex items-center justify-between">
                      Aksi
                      <a href="#">
                        <img
                          class="h-5"
                          src="../../../public/icon/Table-up-and-down-arrow.png"
                          alt="Image up down arrow"
                        />
                      </a>
                    </div>
                  </th>
                </tr>
              </thead>
              <tbody>
                <tr class="h-52">
                  <td colspan="7">
                    <p class="text-gray-800 font-semibold text-lg text-center">
                      Tidak ada daftar truk
                    </p>
                  </td>
                </tr>
              </tbody>
              <tfoot>
                <tr>
                  <th colspan="7">
                    <div class="flex items-center justify-between mt-5 p-2">
                      <div class="flex items-center">
                        <label
                          for="page"
                          class="text-sm text-gray-500 mr-2 font-thin"
                          >Rows per page:
                        </label>
                        <select
                          id="page"
                          class="mb-6 p-1 text-sm text-gray-900 border outline-none rounded-md bg-transparent mt-5"
                        >
                          <option>1</option>
                          <option>10</option>
                          <option>20</option>
                          <option>50</option>
                          <option>100</option>
                        </select>
                      </div>
                      <div class="flex items-center gap-3">
                        <button
                          type="button"
                          class="bg-gray-200 p-2 rounded-lg w-full flex justify-center"
                        >
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke-width="1.5"
                            stroke="currentColor"
                            class="w-5 h-5"
                          >
                            <path
                              stroke-linecap="round"
                              stroke-linejoin="round"
                              d="M15.75 19.5L8.25 12l7.5-7.5"
                            />
                          </svg>
                        </button>

                        <button
                          type="button"
                          class="bg-primary-9 px-4 py-2 text-white rounded-lg w-full"
                        >
                          <p>1</p>
                        </button>
                        <button
                          type="button"
                          class="bg-white p-2 text-primary-9 ring-1 ring-primary-9 rounded-lg w-full"
                        >
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke-width="1.5"
                            stroke="currentColor"
                            class="w-5 h-5"
                          >
                            <path
                              stroke-linecap="round"
                              stroke-linejoin="round"
                              d="M8.25 4.5l7.5 7.5-7.5 7.5"
                            />
                          </svg>
                        </button>
                      </div>
                    </div>
                  </th>
                </tr>
              </tfoot>
            </table>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>


<script lang="ts" setup>
import Navbar from '@/components/navbar/Navbar.vue'
import Sidebar from '@/components/menu-sidebar/SideMenu.vue'
</script>



