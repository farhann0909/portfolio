<script>
export default {
  data() {
    return {
      activeTab: 1,
      items: [
        {
          id: 1,
          name: 'Analisa Kemacetan Kota Bandung',
          imageUrl: require('@/assets/images/Analisa Kemacetan Kota Bandung.png'),
          status: 'Studi untuk menganalisis penyebab kemacetan di Kota Bandung dengan pendekatan data-driven.',
          tech: 'Strategic Management',
          demo: 'https://drive.google.com/file/d/1lLB4N6TnoEO8e3lgpFqTzSI4_IFGvS-f/view?usp=sharing'
        },
        {
          id: 2,
          name: 'Management Strategic PT Bank Aladin Syariah Tbk',
          imageUrl: require('@/assets/images/Management Strategic PT Bank Aladin Syariah Tbk.png'),
          status: 'Strategi manajemen untuk meningkatkan daya saing dan pertumbuhan Bank Aladin Syariah.',
          tech: 'Strategic Management',
          demo: 'https://drive.google.com/file/d/14YhR4AlrqZztECh527d_jhsvTLq9-irB/view?usp=sharing'
        },
        {
          id: 3,
          name: 'Management Strategic PT Telkom Indonesia Tbk',
          imageUrl: require('@/assets/images/Management Strategic PT Telkom Indonesia Tbk.png'),
          status: 'Analisis strategi manajemen untuk mendukung transformasi digital di PT Telkom Indonesia.',
          tech: 'Strategic Management',
          demo: 'https://drive.google.com/file/d/1yPpillfFG7TVwI9qz2n7mx_W23BctJi5/view?usp=sharing'
        },
        {
          id: 4,
          name: 'Business Analysis of Global Superstore',
          imageUrl: require('@/assets/images/Business Analysis of Global Superstore.png'),
          status: 'Analisis bisnis menggunakan dataset Global Superstore untuk meningkatkan efisiensi operasional.',
          tech: 'Data Analyst',
          demo: 'https://drive.google.com/file/d/1MkpfiAhNdufv4kR6rYzT_cMiRFg_p_25/view?usp=sharing'
        },
        {
          id: 5,
          name: 'AlloBank Increasing Active User Strategy',
          imageUrl: require('@/assets/images/AlloBank Increasing Active User with GPS Strategy.png'),
          status: 'Strategi untuk meningkatan active user bagi AlloBank.',
          tech: 'Strategic Management',
          demo: 'https://drive.google.com/file/d/1EHkXXQHog2YXx4xkqkqv3_rLnIXC4AYx/view?usp=sharing'
        },
        {
          id: 6,
          name: 'Wakely Marketing Strategy',
          imageUrl: require('@/assets/images/Wakely Marketing Strategy.png'),
          status: 'Analisis strategi pemasaran produk minuman Wakely.',
          tech: 'Marketing Strategy',
          demo: 'https://drive.google.com/file/d/1uCZbUbPFgU6HKRQKLp7JLh4jU4EhXnW2/view?usp=sharing'
        },
        {
          id: 7,
          name: 'Biteship Business Valuation',
          imageUrl: require('@/assets/images/Biteship Business Valuation.png'),
          status: 'Valuasi bisnis untuk Biteship dengan pendekatan Berkus, Scorecard, dan Risk Factor Method.',
          tech: 'Business Valuation',
          demo: 'https://drive.google.com/file/d/1biteship-valuation/view?usp=sharing'
        },
        {
          id: 8,
          name: 'Bookmart Cyber Security Risk Management',
          imageUrl: require('@/assets/images/Bookmart Cyber Security Risk Management.png'),
          status: 'Manajemen risiko keamanan siber untuk Bookmart.',
          tech: 'Risk Management',
          demo: 'https://drive.google.com/file/d/1OTpIaPyMTkt05FB53nT8EtZI10XnGUEM/view?usp=sharing'
        },
        {
          id: 9,
          name: 'Bike Sharing Dashboard',
          imageUrl: require('@/assets/images/Bike Sharing Dashboard.png'),
          status: 'Dashboard berbasis data untuk menganalisis penggunaan bike sharing.',
          tech: 'Data Analyst',
          demo: 'https://bike-sharing-dashboard-farhan.streamlit.app',
          repo: 'https://github.com/farhann0909/bike-sharing-dashboard'
        }
      ]
    };
  }
};
</script>

<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Past Project Experience</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300">
            Explore the projects I've worked on so far</h4>
        </div>
      </header>
      <section>
        <div>
          <div class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-3 md:gap-3 xl:grid-cols-3 xl:gap-3 2xl:gap-5 fade-zoom-in">
            <div v-for="item in items" :key="item.id">
              <div class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-amber-50 md:gap-3 px-5 py-5 lg:px-5">
                <div class="flex h-12 w-12 items-center justify-center h-full w-full zoom-in">
                  <img :alt="item.name" :src="item.imageUrl" class="drop-shadow-xl rounded rounded-xl">
                </div>
                <div class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg">
                  <div class="title-text font-medium text-secondary">{{ item.name }}</div>
                  <div class="w-full text-left text-[10px] text-[#c1c1c1] md:text-xs lg:text-sm">{{ item.status }}</div>
                  <div class="w-full mt-4 text-normal text-sm text-left text-amber-200">{{ item.tech }}</div>
                  <div class="w-full flex justify-end">
                    <div class="flex cursor-pointer items-end gap-2 text-primary">
                      <a v-if="item.demo" :href="item.demo" target="_blank" rel="noreferrer" title="View finished project" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
                          <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 1 1 2-2h6"></path>
                          <polyline points="15 3 21 3 21 9"></polyline>
                          <line x1="10" y1="14" x2="21" y2="3"></line>
                        </svg>
                      </a>
                      <a v-if="item.repo" :href="item.repo" target="_blank" rel="noreferrer" title="View repository" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
                          <path d="M9 19c-4.418 0-8-3.582-8-8s3.582-8 8-8 8 3.582 8 8c0 3.313-2.691 6-6 6H9m0 0v3m0-3h3"></path>
                        </svg>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.item-card:hover {
  transition: transform 0.3s ease;
  transform: translateY(-8px);
}
svg:hover {
  stroke: #ffdb70;
}
@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
.fade-zoom-in {
  animation: fadeZoomIn 1s ease-in-out;
}
</style>
