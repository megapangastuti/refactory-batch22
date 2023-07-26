<template>
  <div class="flex h-full bg-gray-200">
    <Sidebar />
    <div class="flex flex-col flex-1 overflow-x-hidden">
      <Navbar />
      <main class="flex-1 overflow-x-hidden bg-[#FFFFFF]">
        <div class="px-8 py-4">
          <div class="py-4">
            <div>
              <p class="text-gray-500">
                Konfigurasi /
                <span class="text-gray-800">Data Daftar Truk</span>
              </p>
              <p class="mt-3 text-2xl font-semibold">Data Daftar Truk</p>
              <p class="text-gray-500">Informasi List Daftar truk</p>
            </div>

            <div
              class="flex flex-wrap items-center justify-between my-8 gap-y-4"
            >
              <div
                class="flex items-center w-full px-3 text-lg bg-gray-200 rounded-lg md:w-96"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="w-6 h-6 text-gray-700"
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
                  class="w-full py-3 pl-3 text-base font-thin text-gray-600 bg-gray-200 rounded-lg form-controll text focus:outline-none"
                  placeholder="Cari truk"
                />
              </div>

              <button
                type="button"
                class="flex items-center justify-center h-12 font-semibold text-red-600 bg-white border border-red-600 rounded-lg w-44 hover:bg-red-600 hover:text-white"
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
          </div>

          <section class="min-h-screen mt-8">
            <BaseTable :data="items" :column="headers" />
          </section>
        </div>
      </main>
    </div>
  </div>
</template>

<script lang="ts">
import Navbar from '@/components/navbar/Navbar.vue'
import Sidebar from '@/components/menu-sidebar/SideMenu.vue'
import BaseTable from '@/components/base-table/BaseTable.vue'

export default {
  components: {
    Navbar,
    Sidebar,
    BaseTable
  },

  setup() {
    const items: any[] = Array.from({ length: 50 }).map(() => {
      return {
        id: 'JGCR-2536782',
        jenis: 'Truk Engkel',
        merek: 'Daihatsu',
        tipe: 'Bak Terbuka',
        volume: '8',
        kapasitas: '10000 Kg'
      }
    })

    const headers: any[] = [
      { text: 'ID TRUCK', value: 'id', sortable: true },
      { text: 'Jenis Kendaraan', value: 'jenis', sortable: true },
      { text: 'Mereke', value: 'merek', sortable: true },
      { text: 'Tipe Kendaraan', value: 'tipe', sortable: true },
      { text: 'Volume', value: 'volume', sortable: true },
      { text: 'Kapasitas', value: 'kapasitas', sortable: true },
      { text: 'Aksi', value: 'action' }
    ]

    return { items, headers }
  }
}
</script>


