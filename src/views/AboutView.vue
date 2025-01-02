<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        { id: 1, name: 'MySQL', imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968313.png', status: 'Intermediate' },
        { id: 2, name: 'PostgreSQL', imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968342.png', status: 'Intermediate' },
        { id: 3, name: 'Python', imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968350.png', status: 'Beginner' },
        { id: 4, name: 'HTML', imageUrl: 'https://cdn-icons-png.flaticon.com/512/732/732212.png', status: 'Beginner' },
        { id: 5, name: 'CSS', imageUrl: 'https://cdn-icons-png.flaticon.com/512/732/732190.png', status: 'Beginner' },
      ],
      tools: [
        { id: 1, name: 'DBeaver', imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/DBeaver_logo.svg/2048px-DBeaver_logo.svg.png', status: 'RDBMS' },
        { id: 2, name: 'KNIME', imageUrl: 'https://forum-cdn.knime.com/uploads/default/original/1X/ab3ccf34482a0329361734a18199390177204f15.png', status: 'Data Analytics' },
        { id: 3, name: 'Excel', imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/3/34/Microsoft_Office_Excel_%282019%E2%80%93present%29.svg/2203px-Microsoft_Office_Excel_%282019%E2%80%93present%29.svg.png', status: 'Data Processing' },
        { id: 4, name: 'PowerPoint', imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/1/16/Microsoft_PowerPoint_2013-2019_logo.svg', status: 'Presentation Design' },
        { id: 5, name: 'Canva', imageUrl: 'https://cdnlogo.com/logos/c/41/canva.svg', status: 'Design' },
        { id: 6, name: 'Looker Studio', imageUrl: 'https://www.svgrepo.com/show/354012/looker-icon.svg', status: 'Data Visualization' },
        { id: 7, name: 'Tableau', imageUrl: 'https://cdn.worldvectorlogo.com/logos/tableau-software.svg', status: 'Data Visualization' },
      ],
    };
  },
};
</script>

<template>
  <div class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          About Me &nbsp;
          <div class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left" data-aos-duration="600"></div>
        </div>
      </header>
      <section class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center">
        <div class="flex justify-center">
          <img class="w-9/12 rounded-full mb-3 fadein-up" src="@/assets/images/Foto.jpeg" alt="Foto">
        </div>
        <div class="md:w-7/12">
          <p class="mb-3 md:mb-7 fadein-left fadeins-1">
            Hi everyone! My name is Farhan Aulia Rahman. I am a digital business student at Universitas Padjadjaran with expertise in business development and data analysis. 
            I am passionate about solving problems using data-driven strategies to drive growth and innovation.
          </p>
          <p class="mb-3 fadein-left fadeins-2">
            My experience includes leading projects as a teaching assistant and managing growth strategies in several organizations. 
            My aim is to deliver impactful and sustainable results through collaboration and creativity. 
            Let's connect and explore opportunities to work together.
          </p>
          <div class="mt-4">
            <a
              href="https://drive.google.com/file/d/your-cv-link-here/view?usp=sharing"
              target="_blank"
              class="px-4 py-2 bg-amber-200 text-black font-semibold rounded-lg hover:bg-amber-300 transition-all">
              Download CV
            </a>
          </div>
        </div>
      </section>
    </article>
  </div>

  <!-- Skills Section -->
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          <div class="h-[1px] w-10 bg-amber-200 md:w-20 aos-init aos-animate" data-aos="zoom-in-left" data-aos-duration="600"></div>
          &nbsp; Skills
        </div>
      </header>
      <section>
        <div>
          <ul class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5">
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white" :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 1 }" @click="activeTab = 1">Tech Stack</button>
            </li>
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white" :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 2 }" @click="activeTab = 2">Tools</button>
            </li>
          </ul>
        </div>
        <div v-show="activeTab === 1">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tech" :key="item.id">
              <div class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1" class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]" :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}</div>
                  <div class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">{{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div v-show="activeTab === 2">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tools" :key="item.id">
              <div class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1" class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]" :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}</div>
                  <div class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">{{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>


