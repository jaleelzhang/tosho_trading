<script setup>
  import { ref, computed } from 'vue'
  import { Icon } from '@iconify/vue'

  const lecturers = ref([
    {
      id: 1,
      name: '長田 圭二',
      course: 'エンジニアコース',
      experience: [
        '新卒から約10年間東京の広告代理店に勤務。主にWeb広告の運用、メディアプランニングに従事。',
        '2019年より個人事業にて映像制作を開始。',
        '現在はフリーランスとして大分県を拠点に、企业や店舗のPV・Web広告の企画、撮影、制作を中心に行いながら映画の制作にも携わっている。'
      ],
      message: '何か新しいことに挑戦する時にはそれなりのパワーと、勇気がいると思います。本講座で、仲間と一緒に学んでもらいながら少しでも皆さんの後押しができればと考えてます。一緒に全力で映像 制作を楽しみましょう！'
    },
    {
      id: 2,
      name: '長田 圭二',
      course: 'エンジニアコース',
      experience: [
        '新卒から約10年間東京の広告代理店に勤務。主にWeb広告の運用、メディアプランニングに従事。',
        '2019年より個人事業にて映像制作を開始。',
        '現在はフリーランスとして大分県を拠点に、企业や店舗のPV・Web広告の企画、撮影、制作を中心に行いながら映画の制作にも携わっている。'
      ],
      message: '何か新しいことに挑戦する時にはそれなりのパワーと、勇気がいると思います。本講座で、仲間と一緒に学んでもらいながら少しでも皆さんの後押しができればと考えてます。一緒に全力で映像 制作を楽しみましょう！'
    },
    {
      id: 3,
      name: '長田 圭二',
      course: 'エンジニアコース',
      experience: [
        '新卒から約10年間東京の広告代理店に勤務。主にWeb広告の運用、メディアプランニングに従事。',
        '2019年より個人事業にて映像制作を開始。',
        '現在はフリーランスとして大分県を拠点に、企业や店舗のPV・Web広告の企画、撮影、制作を中心に行いながら映画の制作にも携わっている。'
      ],
      message: '何か新しいことに挑戦する時にはそれなりのパワーと、勇気がいると思います。本講座で、仲間と一緒に学んでもらいながら少しでも皆さんの後押しができればと考えてます。一緒に全力で映像 制作を楽しみましょう！'
    }
  ])

  const activeIndex = ref(0)
  const cardWidth = 813 
  const gap = 30 

  const trackStyles = computed(() => ({
    transform: `translateX(${-activeIndex.value * (cardWidth + gap)}px)`,
  }))

  const next = () => { if (activeIndex.value < lecturers.value.length - 1) activeIndex.value++ }
  const prev = () => { if (activeIndex.value > 0) activeIndex.value-- }
</script>

<template>
  <div class="max-w-container mx-auto w-full">
    <header class="bg-white w-full sticky top-0 z-[100] shadow-sm">
      <nav class="flex justify-between items-center h-16 md:h-20 px-5 md:px-10 mx-auto">
        
        <div class="w-24 md:w-32 flex-shrink-0">
          <img src="./assets/logo.svg" alt="logo" class="w-full h-auto">
        </div>

        <div class="hidden md:flex items-center gap-6 lg:gap-8 ml-auto mr-8">
          <a href="#" class="nav-link whitespace-nowrap text-[14px] font-bold">選ばれる理由</a>
          <a href="#" class="nav-link whitespace-nowrap text-[14px] font-bold">受講者の実績</a>
          <a href="#" class="nav-link whitespace-nowrap text-[14px] font-bold">コース・料金</a>
          <a href="#" class="nav-link whitespace-nowrap text-[14px] font-bold">受講の流れ</a>
          <a href="#" class="nav-link whitespace-nowrap text-[14px] font-bold">よくあるご質問</a>
        </div>

        <div class="flex items-center">
          <button class="hidden md:flex items-center py-[10.68px] px-4 bg-linear-to-r from-brand-pink-dark to-brand-pink-light rounded-[2.05px] transition hover:brightness-110">
            <span class="text-white text-[12px] leading-none font-bold tracking-[0.05em]">無料相談に参加する</span>
            <Icon icon="cuida:caret-right-outline" class="text-white text-[10px] ml-1" />
          </button>

          <button class="md:hidden flex items-center p-1">
            <Icon icon="line-md:menu" class="text-[28px] text-[#D17E66]" />
          </button>
        </div>
      </nav>
    </header>

    <section class="md:h-[676px] h-[474px] w-full hero-bg bg-right bg-no-repeat bg-cover flex flex-col md:gap-[15px] gap-[8.14px] relative">
      <div class="md:py-[10px] py-[5.11px] md:px-[25px] px-[12.77px] ml-[12.27px] md:ml-[89.76px] md:mt-[114px] mt-[30px] bg-[#333333] self-start md:gap-[15.94px] gap-[8.14px] inline-block -skew-x-5 z-10">
        <span class="md:text-[54px] text-[28px] font-bold tracking-[0.04em] leading-none text-white inline-block">
          完全未経験<span class="traking-[0.06em]">から</span>
        </span>
      </div>
      <div class="md:py-[5px] py-[5.11px] md:px-[25px] px-[12.77px] ml-[12.27px] md:ml-[89.76px] bg-[#333333] self-start md:gap-[15.94px] gap-[8.14px] inline-block -skew-x-5 z-10">
        <span class="md:text-[54px] text-[28px] font-bold tracking-[0.03em] leading-none text-white inline-block">
          最短2か月で実績を持<span class="traking-[0.08em]">てる</span>
        </span>
      </div>
      <div class="md:py-[10px] py-[5.11px] md:px-[25px] px-[12.77px] ml-[12.27px] md:ml-[89.76px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light self-start md:gap-[15.94px] gap-[8.14px] inline-block -skew-x-5 z-10">
        <span class="md:text-[54px] text-[24px] font-bold leading-none text-white inline-block">プログラミングスクール</span>
      </div>

      <img src="./assets/fv23 1.svg" class="md:w-[576px] w-[265px] md:h-[607px] h-[279px] absolute bottom-[0px] md:right-[40px] md:left-auto left-[18px] z-0" />

      <div class="flex md:flex-row flex-col md:items-start items-end mt-[30px] md:ml-[89.76px] mr-[25px] gap-[10px] z-10">
        <div class="md:w-[204px] w-[126.99px] md:h-[113px] h-[64.34px] md:shadow-[2px_2px_10.5px_2px_rgba(0,0,0,0.1)] shadow-[1.25px_1.25px_6.54px_1.25px_rgba(0,0,0,0.1)] bg-white flex flex-col items-center justify-center font-bold">
            <span class="md:text-[18px] text-[11.21px] tracking-[0.05em] leading-[1.1]">卒業生限定案件数</span>
            <div class="flex items-baseline leading-none mt-1">
              <span class="md:text-[20px] text-[12.45px]">年間</span>
              <span class="md:text-[40px] text-[24.9px]">1</span>
              <span class="md:text-[26px] text-[16.19px]">万</span>
              <span class="md:text-[20px] text-[12.45px]">件以上</span>
            </div>
        </div>

        <div class="md:w-[204px] w-[126.99px] md:h-[113px] h-[64.34px] md:shadow-[2px_2px_10.5px_2px_rgba(0,0,0,0.1)] shadow-[1.25px_1.25px_6.54px_1.25px_rgba(0,0,0,0.1)] bg-white flex flex-col items-center justify-center text-[14px] font-bold">
            <span class="md:text-[18px] text-[11.21px] leading-[1.1] tracking-[0em]">入会から卒業まで</span>
            <div class="flex items-baseline leading-none mt-1">
              <span class="md:text-[20px] text-[12.45px]">最短</span>
              <span class="md:text-[40px] text-[24.9px]">1</span>
              <span class="md:text-[20px] tracking-[-0.1em] text-[12.45px]">ヶ月</span>
            </div>
        </div>

        <div class="md:w-[204px] w-[126.99px] md:h-[113px] h-[64.34px] md:shadow-[2px_2px_10.5px_2px_rgba(0,0,0,0.1)] shadow-[1.25px_1.25px_6.54px_1.25px_rgba(0,0,0,0.1)] bg-white flex flex-col items-center justify-center text-[14px] font-bold">
          <span class="text-[18px]">業界最安級</span>
          <div class="flex items-baseline leading-none mt-1">
              <span class="md:text-[18px] text-[11.21px] leading-[1.2] tracking-[-0.1em]">月々</span>
              <span class="md:text-[40px] text-[24.9px] ml-1">4</span>
              <span class="md:text-[17.32px] text-[10.78px]">,</span>
              <span class="md:text-[40px] text-[24.9px]">583</span>
              <div class="flex flex-col ml-1 self-end pb-1 leading-tight">
                <span class="md:text-[12px] text-[7.47px]">(税込)</span>
                <span class="md:text-[14px] text-[8.72px]">円～</span>
              </div>
          </div>
        </div>
      </div>
    </section>

    <section class="w-full bg-white relative overflow-hidden md:h-[1500px]">
      <img 
        src="./assets/logo-bg-pattern.svg" 
        class="absolute md:top-[-290px] top-[60px] left-[-25px] md:left-[-150px] w-[281.24px] md:w-[1332.87px] h-[216.38px] md:h-[1025.48px] opacity-85 pointer-events-none rotate-[-2deg]"
        alt="background pattern"
      />

      <div class="w-full p-[0px] md:p-[50px] flex justify-center items-center relative z-10">
        <div class="hero-bg bg-white bg-cover bg-no-repeat md:rounded-[5px] overflow-hidden w-full md:w-[507px]">
          <div class="py-[22.19px] md:py-[30px] px-[44.38px] md:px-[60px] gap-[7.4px] md:gap-[10px] flex flex-col bg-black/66 flex items-center">
            <span class="text-[16px] md:text-[20px] text-white font-bold leading-none">＼ 最短30秒でかんたん予約！／</span>
            <button class="relative w-[286.24px] md:w-[387px] h-[53.25px] md:h-[72px] flex justify-center items-center py-[19.23px] md:py-[26px] px-[13.79px] md:px-[20px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light rounded-[3.7px] md:rounded-[5px] transition hover:brightness-110 shadow-[1.48px_1.48px_0_0_rgba(0,0,0,0.25)] md:shadow-[2px_2px_0_0_rgba(0,0,0,0.25)]">
              <span class="text-[18px] md:text-[24px] font-bold text-white tracking-[0.05em] leading-none shadow-[0_0_1.55px_0_rgba(0,0,0,0.49)] md:shadow-[0_0_2.1px_0_rgba(0,0,0,0.49)]">無料相談に参加する</span>
              <Icon class="absolute text-[18px] md:text-[24px] font-bold text-white right-[10px] md:right-[15px]" icon="cuida:caret-right-outline"/>
            </button>
          </div>
        </div>
      </div>

      <div class="flex flex-col md:flex-row w-full mt-10 md:mt-[50px] relative items-end md:items-end md:justify-center md:mb-[120px]">
        <img src="./assets/computer.svg" class="absolute -left-8 top-10 md:top-3 w-[191px] md:w-[583.25px] h-[151px] md:h-[461.36px] rotate-[2deg] z-20 md:left-[0] md:mt-[-40px]" />
        <div class="w-full md:w-auto flex flex-col md:items-start items-end leading-none tracking-[0.05em] gap-[8px] md:gap-[40px] pt-[20px] pr-[10%] md:ml-[30%] font-bold">
          <div class="flex items-baseline">
            <span class="md:text-[48px] text-[30px]">びるどるスクール</span>
            <span class="md:text-[36px] text-[22px]">とは？</span>
          </div>
          <div class="flex flex-col md:items-start items-end justify-center md:gap-[10px] gap-[8px]">
            <span class="md:text-[32px] text-[18.13px] leading-[1.6]">卒業後すぐに実績を積める</span>
            <div class="flex items-center md:gap-[10px]">
              <img src="./assets/big_logo.svg" class="md:w-[201px] w-[114.1px] md:h-[52px] h-[29.42px]" />
              <span class="md:text-[32px] text-[18.13px] leading-[1.6]">が運営する</span>
            </div>
            <span class="md:text-[32px] text-[18.13px] leading-[1.6]">プログラミングスクール</span>
          </div>
        </div>
      </div>

      <div class="flex flex-col items-center leading-none tracking-[0.05em] gap-[30px] md:gap-[50px] px-[10px] md:px-[100px] py-[70px] md:py-[10px]">
        <span class="text-[48px] font-bold text-text-dark">受講者の実績</span>
        <div class="flex flex-col md:flex-row items-center gap-10 text-white">
          <div class="flex flex-col w-full md:w-[367px] p-[30px] gap-5 bg-linear-to-r from-brand-pink-dark to-brand-pink-light">
            <div class="relative">
              <img src="./assets/xsan.svg">
              <span class="bg-black absolute bottom-0 text-medium leading-[1.5]">N.Hさん</span>
            </div>
            <span class="text-[18px] font-bold leading-none tracking-[0.05em]">卒業後2ヶ月で初案件獲得！<br>半年で月収50万円に</span>
            <span class="text-medium leading-[1.5em]">一度別のプログラミングスクールで挫折してしまいましたが、びるどるスクールで「稼ぐために本当に必要なこと」を教わることができました。</span>
            <span class="flex justify-end text-medium leading-[1.5em]">30代男性/フリーランス</span>
          </div>
          <div class="flex flex-col w-full md:w-[367px] p-[30px] gap-5 bg-linear-to-r from-brand-pink-dark to-brand-pink-light">
            <div class="relative">
              <img src="./assets/xsan.svg">
              <span class="bg-black absolute bottom-0 text-medium leading-[1.5]">S.Rさん</span>
            </div>
            <span class="text-[18px] font-bold leading-none tracking-[0.05em]">卒業後2ヶ月で初案件獲得！<br>半年で月収50万円に</span>
            <span class="text-medium leading-[1.5em]">進め方などで困ったとき、「サポートセンター」が手厚く支援してくれたので、難易度の高い案件にもチャレンジでき、大きなキャリアアップに繋がりました。</span>
            <span class="flex justify-end text-medium leading-[1.5em]">20代男性/フリーランス</span>
          </div>

          <div class="flex flex-col w-full md:w-[367px] p-[30px] gap-5 bg-linear-to-r from-brand-pink-dark to-brand-pink-light">
            <div class="relative">
              <img src="./assets/xsan.svg">
              <span class="bg-black absolute bottom-0 text-medium leading-[1.5]">K.Iさん</span>
            </div>
            <span class="text-[18px] font-bold leading-none tracking-[0.05em]">家事・育児と両立し、<br>未経験から2ヶ月で初案件獲得！</span>
            <span class="text-medium leading-[1.5em]">びるどるスクールはただプログラミングを学ぶのではなく、実際の過去の案件に基づいたカリキュラムを経験できるのが大きな利点だと思います。</span>
            <span class="flex justify-end text-medium leading-[1.5em]">30代女性/副業</span>
          </div>
        </div>
      </div>
    </section>

    <section class="chat-bg bg-cover bg-no-repeat bg-center w-full py-[70px] md:py-[100px] gap-[30px] md:gap-[40px] flex flex-col items-center relative">
      <div class="absolute inset-0 bg-black/60 z-0"></div>
      <div class="flex items-center gap-[20px] md:gap-[42px] font-medium leading-[1.4] relative z-10">
        <div class="bg-white  px-[20px] py-[17px] gap-[10px] flex flex-col items-center font-medium text-[14px] md:text-[16px] leading-[1.4] relative shadow-[2px_2px_0_0_rgba(0,0,0,0,0.25)]">
          <span class="">未経験からでも</span>
          <span>大丈夫？</span>
          <img src="./assets/vector.svg" class="absolute left-1/2 -translate-x-1/2 bottom-[-1px] translate-y-2.5" alt="" />
        </div>
        <div class="bg-white px-[20px] py-[17px] gap-[10px] flex flex-col items-center font-medium text-[14px] md:text-[16px] leading-[1.4] relative shadow-[2px_2px_0_0_rgba(0,0,0,0,0.25)]">
          <span class="">仕事しながらでも</span>
          <span>できる？</span>
          <img src="./assets/vector.svg" class="absolute left-1/2 -translate-x-1/2 bottom-[-1px] translate-y-2.5" alt="" />
        </div>
      </div>
      <div class="text-white gap-[7.41px] md:gap-[10px] flex flex-col items-center font-bold tracking-[0.05em] leading-none relative z-10">
        <span class="md:text-[36px] text-[30px]">無料相談実施中！</span>
        <span class="md:text-[20px]text-[16px] leading-[1.8]">プロのカウンセラーになんでも相談可能！</span>
      </div>
      <div class="md:py-[30px] md:px-[60px] gap-[7.4px] md:gap-[10px] flex flex-col flex items-center relative z-10">
        <span class="text-[14.79px] md:text-[20px] text-white font-bold leading-none">＼ 最短30秒でかんたん予約！／</span>
        <button class="relative w-[286.24px] md:w-[387px] h-[53.25px] md:h-[72px] flex justify-center items-center py-[19.23px] md:py-[26px] px-[14.79px] md:px-[20px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light rounded-[3.7px] md:rounded-[5px] transition hover:brightness-110 shadow-[1.48px_1.48px_0_0_rgba(0,0,0,0.25)] md:shadow-[2px_2px_0_0_rgba(0,0,0,0.25)]">
          <span class="text-[17.75px] md:text-[24px] font-bold text-white tracking-[0.05em] leading-none shadow-[0px_0px_1.55px_0px_rgba(0,0,0,0.49)] md:shadow-[0_0_2.1px_0_rgba(0,0,0,0.49)]">無料相談に参加する</span>
          <Icon class="absolute text-[17.75px] md:text-[24px] font-bold text-white right-[10px] md:right-[15px]" icon="cuida:caret-right-outline"/>
        </button>
      </div>
    </section>

    <section class="hero-bg bg-right bg-cover bg-no-repeat flex flex-col items-center py-[70px] md:py-[100px] gap-[30px] md:gap-[50px] md:h-[1800px] font-bold">
      <div class="text-[20px] md:text-[36px] tracking-[0.05em] [text-shadow:0_0_8px_rgba(255,255,255,1),0_0_8px_rgba(255,255,255,1)] flex flex-col items-center">
        <span class="">びるどるスクールが選ばれる</span>
        <span class="text-[30px] md:text-[64px] md:mt-[-10px]">3つの理由</span>
      </div>

      <div class="flex flex-col items-start relative gap-[10px] w-full md:h-[443.47px]">
        <span class="font-['Akshar'] absolute top-[530px] md:top-[350px] left-[25.04px] md:left-[250px] z-0 text-[58px] md:text-[174.81px] text-[#F7F7F7] leading-[139.85px] font-medium tracking-[0em] opacity-90 -skew-x-5">Introduction</span>
        <div class="w-[335.56px] md:w-[647px] h-[250.71px] md:h-[315px] md:absolute ml-[0px] mt-[37.48px] md:top-[50px] computer-bg bg-cover bg-left bg-no-repeat overflow-hidden border-[1px] border-black">
          <div class="md:absolute w-full h-full z-0 bg-[#E03551]/90"></div>
        </div>
        <img src="./assets/computer2.svg" class="absolute z-10 top-[0px] left-[26.67px] md:left-[252px] w-[333.33px] md:w-[450px] h-[262.37px] md:h-[315px]" />
        <div class="md:absolute top-[298.19px] md:top-[25px] left-[0px] md:left-[702px] gap-[10px] flex items-center">
          <div class="h-[1px] w-[273.59px] md:w-[333px] bg-[#333333]"></div>
          <span class="md:ml-[10px] font-bold text-[16px] italic text-[#333333] leading-[40px]">
            POINT <span class="text-[24px] leading-[40px] font-medium">01</span>
          </span>
        </div>
        <div class="md:absolute z-10 md:left-[736px] ml-[26px] md:top-[90px] w-[320.22px] md:w-[375.19px] h-[248px] md:h-[219px] gap-[15px] md:gap-[16px] flex flex-col items-center">
          <span class="font-bold text-[20px] md:text-[24px] leading-[1.2] tracking-[0.05em]">卒業後は「びるどる」から 案件を優先紹介</span>
          <span class="font-medium text-[16px] leading-[1.8] tracking-[0em]">びるどるスクールは、Web制作サービス「びるどる」の運営するプログラミングスクールです。
            卒業後はびるどるの「認定パートナー」として、エンジニア案件を優先的に紹介してもらうことが可能です。</span>
        </div>
      </div>

      <div class="flex flex-col relative items-end gap-[10px] w-full md:h-[443.47px]">
        <span class="font-['Akshar'] absolute top-[530px] md:top-[350px] left-[25.04px] md:left-[250px] z-0 text-[58px] md:text-[174.81px] text-[#F7F7F7] leading-[139.85px] font-medium tracking-[0em] opacity-90 -skew-x-5">Curriculum</span>
        <div class="w-[335.56px] md:w-[647px] h-[250.71px] md:h-[315px] md:absolute mr-[0px] mt-[37.48px] md:top-[50px] computer-bg_3 bg-cover bg-left bg-no-repeat overflow-hidden border-[1px] border-black">
          <div class="md:absolute w-full h-full z-0 bg-[#E03551]/90"></div>
        </div>
        <img src="./assets/computer3.svg" class="absolute z-10 top-[0px] right-[26.67px] md:left-[738px] w-[333.33px] md:w-[450px] h-[262.37px] md:h-[315px]" />
        <div class="md:absolute top-[298.19px] md:top-[25px] left-[0px] md:left-[329px] gap-[10px] flex items-center">
          <span class="font-bold text-[16px] italic text-[#333333] leading-[40px]">
            POINT <span class="text-[24px] leading-[40px] font-medium">02</span>
          </span>
          <div class="h-[1px] w-[273.59px] md:w-[333px] bg-[#333333] md:ml-[10px]"></div>
        </div>
        <div class="md:absolute z-10 md:left-[329px] mr-[26px] top-[352.09px] md:top-[90px] w-[320.22px] md:w-[375.19px] h-[248px] md:h-[219px] gap-[15px] md:gap-[16px] flex flex-col items-center">
          <span class="font-bold text-[20px] md:text-[24px] leading-[1.2] tracking-[0.05em]">案件をもとにしたカリキュラムで 実践的スキルを身に着けて 即戦力エンジニアへ</span>
          <span class="font-medium text-[16px] leading-[1.8] tracking-[0em]">カリキュラムは「びるどる」が過去実際に受注した案件をもとに作成された超実践的な内容です。
            そのため、卒業後は学んだ内容をそのまま活かしてすぐに「びるどる」の案件を受けられます。</span>
        </div>
      </div>

      <div class="flex flex-col relative items-start gap-[10px] w-full md:h-[443.47px]">
        <span class="font-['Akshar'] absolute top-[530px] md:top-[350px] left-[25.04px] md:left-[250px] z-0 text-[58px] md:text-[174.81px] text-[#F7F7F7] leading-[139.85px] font-medium tracking-[0em] opacity-90 -skew-x-5">Support Mentor</span>
        <div class="w-[335.56px] md:w-[647px] h-[250.71px] md:h-[315px] md:absolute ml-[0px] mt-[37.48px] md:top-[50px] computer-bg bg-cover bg-left bg-no-repeat overflow-hidden border-[1px] border-black">
          <div class="md:absolute w-full h-full z-0 bg-[#E03551]/90"></div>
        </div>
        <img src="./assets/computer4.svg" class="absolute z-10 top-[0px] left-[26.67px] md:left-[252px] w-[333.33px] md:w-[450px] h-[262.37px] md:h-[315px]" />
        <div class="md:absolute top-[298.19px] md:top-[25px] right-[0px] md:left-[702px] gap-[10px] flex items-center">
          <div class="h-[1px] w-[273.59px] md:w-[333px] bg-[#333333]"></div>
          <span class="md:ml-[10px] font-bold text-[16px] italic text-[#333333] leading-[40px]">
            POINT <span class="text-[24px] leading-[40px] font-medium">03</span>
          </span>
        </div>
        <div class="md:absolute z-10 md:left-[736px] ml-[26px] top-[352.09px] md:top-[90px] w-[320.22px] md:w-[375.19px] h-[248px] md:h-[219px] gap-[15px] md:gap-[16px] flex flex-col items-center">
          <span class="font-bold text-[20px] md:text-[24px] leading-[1.2] tracking-[0.05em]">専属メンターが入学から稼げるまで伴走</span>
          <span class="font-medium text-[16px] leading-[1.8] tracking-[0em]">入学してから稼げるようになるまで、専属のメンターがマンツーマンで伴走。
            挫折せずに最後まで学習できるよう、全力でサポートいたします。</span>
        </div>
      </div>
    </section>

    <section class="pt-[100px] pb-[50px] px-[5px] w-full flex flex-col items-center relative">
      <div class="relative md:mt-[50px] w-full md:w-[958px] h-auto md:h-[432px] border-[6px] border-[#E03651] pt-[60px] flex flex-col items-start border-[1px]">
        <div class="absolute -top-[35px] left-1/2 -translate-x-1/2 bg-white px-[20px] whitespace-nowrap flex flex-col items-center">
            <span class="font-bold md:text-[36px] text-[30px] leading-none tracking-[0.05em]">卒業生専用の</span>
            <span class="font-bold md:text-[48px] text-[30px] leading-none tracking-[0.05em]">サポートセンター</span>
        </div>
        <div class="w-[200px] md:w-[770px] h-[252px] md:h-[136px] flex flex-wrap items-center gap-[8px] md:gap-[10px] z-10 md:mt-[15px] ml-[10px]">
          <div class="rounded-[3.91px] md:rounded-[5px] bg-[#ECECEC] p-[8px] md:py-[8px] md:px-[15px] gap[4.96px] md:gap-[6px] flex items-start">
            <img src="./assets/Vector3.svg" class="mt-[5.47px] mr-[3px]"/>
            <span class="font-medium text-[12px] md:text-[15px] leading-[1.5] tracking-[0em] text-[#555555]">依頼が複雑で<br>最適な制作手順を質問したい</span>
          </div>
          <div class="rounded-[3.91px] rounded-[5px] bg-[#ECECEC] p-[8px] md:py-[8px] md:px-[15px] gap[4.96px] md:gap-[6px] flex items-start">
            <img src="./assets/Vector3.svg" class="mt-[5.47px] mr-[3px]"/>
            <span class="font-medium text-[12px] md:text-[15px] leading-[1.5] tracking-[0em] text-[#555555]">デザインで迷ってしまい<br>相談したい</span>
          </div>
          <div class="rounded-[3.91px] rounded-[5px] bg-[#ECECEC] p-[8px] md:py-[8px] md:px-[15px] gap[4.96px] md:gap-[6px] flex items-start">
            <img src="./assets/Vector3.svg" class="mt-[5.47px] mr-[3px]"/>
            <span class="font-medium text-[12px] md:text-[15px] leading-[1.5] tracking-[0em] text-[#555555]">難しいコーディングが必要で<br>アドバイスがほしい</span>
          </div>
          <div class="rounded-[3.91px] rounded-[5px] bg-[#ECECEC] p-[8px] md:py-[8px] md:px-[15px] gap[4.96px] md:gap-[6px] flex items-start">
            <img src="./assets/Vector3.svg" class="mt-[5px] mr-[3px]"/>
            <span class="font-medium text-[12px] md:text-[15px] leading-[1.5] tracking-[0em] text-[#555555]">バックエンドの開発について<br>相談したい</span>
          </div>
          <div class="rounded-[3.91px] rounded-[5px] bg-[#ECECEC] p-[8px] md:py-[8px] md:px-[15px]gap[4.96px] md:gap-[6px] flex items-start">
            <img src="./assets/Vector3.svg" class="mt-[5.47px] mr-[3px]"/>
            <span class="font-medium text-[12px] md:text-[15px] leading-[1.5] tracking-[0em] text-[#555555]">納品物にエラーが出てしまい<br>修正箇所を知りたい</span>
          </div>
          <div class="flex flex-col items-start justify-end">
            <span class="text-[14px] md:text-[20px] leading-[1.5] tracking-[0.03em]">etc...</span>
          </div>
        </div>
        <img src="./assets/anunnsu.svg" class="absolute top-[30px] md:top-[-60px] right-[0%] md:right-[0px] md:left-[750px] z-1" />
        <button class="mt-[100px] w-[90%] md:w-[70%] ml-[5%] md:ml-[15%] md:mt-[30px] flex justify-center items-center px-[10px] md:px-[15px] py-[5px] md:py-[10px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light transition hover:brightness-110 gap-[10px] z-10">
          <span class="text-[18px] md:text-[20px] font-bold text-white tracking-[0.03em] md:tracking-[0.05em] leading-[1.5]">卒業後に「びるどる」から受注した案件で制作で困った場合</span>
        </button>
        <div class="bg-[#F8F8F8] w-full md:h-[171px] z-0 flex items-end mt-[-30px] md:mt-[-40px]">
          <div class="bg-[#FFF1F3] w-full h-[228px] md:h-[158px] z-10 flex flex-col items-center justify-center gap-[15px] md:gap-[5px]">
            <div class="flex flex-col md:flex-row items-center justify-center font-bold leading-[1.5] tracking-[0.05em] text-[#E03651] mt-[50px] md:mt-[40px] w-[329px] md:w-full">
              <span class="text-[32px]">完全無料で</span>
              <div>
                <span class="text-[32px]">永久に使用可能</span>
                <span class="text-[32px] md:text-[28px]">です！</span>
              </div>
            </div>
            <div class="flex flex-col md:flex-row items-center justify-center w-[329px] md:w-full">
              <span class="text-[16px] md:text-[20px] leading-[1.5] font-medium tracking-[0em] text-[#333333]">制作について何でも相談できるため、</span>
              <span class="text-[16px] md:text-[20px] leading-[1.5] font-medium tracking-[0em] text-[#333333]">卒業後も安心して案件を受けられます。</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="py-[70px] md:py-[100px] overflow-hidden bg-white gap-[30px] ml-[10px] md:ml-[0px] relative">
      <div class="w-full md:mb-[60px] flex justify-center items-end md:px-5 relative">
        <div class="flex">
          <h2 class="font-bold text-[30px] md:text-[48px] leading-none tracking-[0.05em] text-[#333]">講師紹介</h2>
        </div>
      </div>

      <div class="flex justify-center mt-[200px] md:mt-[0px] w-full">
        <div 
          :style="trackStyles" 
          class="flex gap-[30px] transition-transform duration-500 ease-out"
        >
          <div 
            v-for="(item, index) in lecturers" 
            :key="item.id"
            :class="index === activeIndex ? 'opacity-100 scale-100' : 'opacity-100 scale-100'"
            class="flex-shrink-0 transition-all duration-500 origin-center"
          >
            <div class="relative w-full md:w-[909px] h-[434px] md:h-[413px] flex items-end">
              
              <div class="absolute top-0 left-[16px] md:left-[50px] w-[calc(100vw-32px)] md:w-[813px] h-[376px] md:h-[389px] border-[1px] border-[#E03551] -z-1"></div>

              <div :class="item.bgClass" class="relative w-[calc(100vw-16px)] md:w-[813px] h-[423px] md:h-[389px] computer-bg_5 bg-cover bg-center py-[30px] px-[15px] md:p-[40px] gap-[10px] box-border">
                <div class="absolute inset-0 bg-[#E03551]/90 z-0"></div>

                <div class="relative z-10 w-full md:w-[553px] text-white leading-[1] tracking-[0.05em]">
                  <div class="font-bold text-[20px] md:text-[24px] mb-2">
                    {{ item.name }}先生 <span class="mx-2">/</span> {{ item.course }}
                  </div>
                  
                  <div class="h-[1px] w-full bg-white/50 mb-2"></div>

                  <div class="mb-2 gap-[5px]">
                    <h4 class="font-bold text-[16px] mb-2">経歴</h4>
                    <div class="flex flex-col gap-1">
                      <div v-for="exp in item.experience" :key="exp" class="flex items-start gap-2">
                        <div class="w-[8px] h-[8px] bg-white rotate-45 mt-[6px] flex-shrink-0"></div>
                        <p class="text-[14px] leading-[1.5] opacity-90">{{ exp }}</p>
                      </div>
                    </div>
                  </div>

                  <div>
                    <h4 class="font-bold text-[16px] mb-1">メッセージ</h4>
                    <p class="text-[14px] leading-[1.6]">{{ item.message }}</p>
                  </div>
                </div>

                <img 
                  src="./assets/photograper.svg" 
                  class="absolute top-[-180px] md:top-[50px] right-1/2 translate-x-1/2 md:translate-x-0 md:-right-[100px] md:top-[50px] w-[216px] md:w-[300px] h-[198px] md:h-[275px] z-20 pointer-events-none" 
                />
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="flex justify-center gap-3 mt-[50px]">
        <button 
          v-for="(_, index) in lecturers" 
          :key="index"
          @click="activeIndex = index"
          :class="index === activeIndex ? 'bg-[#E03651] w-8' : 'bg-gray-300 w-3'"
          class="h-3 rounded-full transition-all duration-300"
        ></button>
      </div>

      <div class="w-full flex flex-col relative md:absolute md:top-[100px]" >
        <div class="flex absolute top-[15px] md:top-[0px] right-1/2 md:right-[200px] translate-x-1/2">
            <button 
              @click="prev"
              :disabled="activeIndex === 0"
              :class="activeIndex === 0 ? 'opacity-30 cursor-not-allowed' : 'hover:bg-red-50'"
              class="w-[50px] h-[50px] border-[2px] border-[#E03651] flex items-center justify-center transition-colors"
            >
              <Icon icon="cuida:caret-left-outline" class="w-[24px] h-[24px] text-[#E03651]" />
            </button>
            <button 
              @click="next" 
              :disabled="activeIndex === lecturers.length - 1"
              :class="activeIndex === lecturers.length - 1 ? 'opacity-30 cursor-not-allowed' : 'hover:bg-red-50'"
              class="w-[50px] h-[50px] border-[2px] border-[#E03651] -ml-[2px] flex items-center justify-center transition-colors"
            >
              <Icon icon="cuida:caret-right-outline" class="w-[24px] h-[24px] text-[#E03651]" />
            </button>
          </div>
        </div>
    </section>

    <section class="chat-bg bg-cover bg-no-repeat bg-center w-full py-[70px] md:py-[100px] mt-[50px] md:mt-[0px] gap-[30px] md:gap-[40px] flex flex-col items-center relative">
      <div class="absolute inset-0 bg-black/60 z-0"></div>
      <div class="flex items-center gap-[20px] md:gap-[42px] font-medium leading-[1.4] relative z-10">
        <div class="bg-white  px-[20px] py-[17px] gap-[10px] flex flex-col items-center font-medium text-[14px] md:text-[16px] leading-[1.4] relative shadow-[2px_2px_0_0_rgba(0,0,0,0,0.25)]">
          <span class="">未経験からでも</span>
          <span>大丈夫？</span>
          <img src="./assets/vector.svg" class="absolute left-1/2 -translate-x-1/2 bottom-[-1px] translate-y-2.5" alt="" />
        </div>
        <div class="bg-white px-[20px] py-[17px] gap-[10px] flex flex-col items-center font-medium text-[14px] md:text-[16px] leading-[1.4] relative shadow-[2px_2px_0_0_rgba(0,0,0,0,0.25)]">
          <span class="">仕事しながらでも</span>
          <span>できる？</span>
          <img src="./assets/vector.svg" class="absolute left-1/2 -translate-x-1/2 bottom-[-1px] translate-y-2.5" alt="" />
        </div>
      </div>
      <div class="text-white gap-[7.41px] md:gap-[10px] flex flex-col items-center font-bold tracking-[0.05em] leading-none relative z-10">
        <span class="md:text-[36px] text-[30px]">無料相談実施中！</span>
        <span class="md:text-[20px]text-[16px] leading-[1.8]">プロのカウンセラーになんでも相談可能！</span>
      </div>
      <div class="md:py-[30px] md:px-[60px] gap-[7.4px] md:gap-[10px] flex flex-col flex items-center relative z-10">
        <span class="text-[14.79px] md:text-[20px] text-white font-bold leading-none">＼ 最短30秒でかんたん予約！／</span>
        <button class="relative w-[286.24px] md:w-[387px] h-[53.25px] md:h-[72px] flex justify-center items-center py-[19.23px] md:py-[26px] px-[14.79px] md:px-[20px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light rounded-[3.7px] md:rounded-[5px] transition hover:brightness-110 shadow-[1.48px_1.48px_0_0_rgba(0,0,0,0.25)] md:shadow-[2px_2px_0_0_rgba(0,0,0,0.25)]">
          <span class="text-[17.75px] md:text-[24px] font-bold text-white tracking-[0.05em] leading-none shadow-[0px_0px_1.55px_0px_rgba(0,0,0,0.49)] md:shadow-[0_0_2.1px_0_rgba(0,0,0,0.49)]">無料相談に参加する</span>
          <Icon class="absolute text-[17.75px] md:text-[24px] font-bold text-white right-[10px] md:right-[15px]" icon="cuida:caret-right-outline"/>
        </button>
      </div>
    </section>

    <section class="flex flex-col items-center py-[70px] md:py-[100px] gap-[40px]">

      <span class="font-bold text-[30px] md:text-[48px] leading-none tracking-[0.05em]">コース・料金</span>

      <div class="flex flex-col md:flex-row items-start md:itmes-center md:justify-center gap-[30px] w-full px-[20px]">
        <div class="w-full md:w-[385px] shadow-[2px_2px_4px_0px__rgba(0,0,0,0.25)] shadow-[2px_2px_10px_0_rgba(0,0,0,0.1)] bg-white">
          <div class="w-full h-[10px] bg-gradient-to-r from-[#F35871] to-[#E03651]"></div>
          <div class="px-[15px] md:px-[30px] py-[35px] flex flex-col gap-[20px]">
            <div class="flex flex-col items-center">
              <div class="font-bold tracking-[0.05em] leading-none bg-gradient-to-b from-[#F35871] to-[#E03651] bg-clip-text text-transparent">
                <span class="text-[30px] md:text-[36px]">短期</span>
                <span class="text-[28px] md:text-[32px]">コース</span>
              </div>
            </div>

            <div class="px-[25px] md:px-[15px] py-[10px] md:py-[12px] bg-[#F6F6F6] flex items-center justify-between leading-none">
              <div class="flex items-center justify-center gap-[10px] md:gap-[20px]">
                <div class="px-[5px] py-[2px] bg-gradient-to-r from-[#E03651] to-[#F35871] shrink-0">
                  <span class="font-bold text-[14px] text-white">料金</span>
                </div>
                <div class="flex items-baseline gap-[2px] md:gap-[5px]">
                  <span class="font-bold text-[36px]">10</span>  
                  <span class="font-bold text-[20px]">万円</span>
                </div>
              </div>
              <div class="flex items-center gap-[10px] md:gap-[20px]">
                <div class="px-[5px] py-[2px] bg-gradient-to-r from-[#F35871] to-[#E03651] shrink-0">
                  <span class="font-bold text-[14px] text-white">学習期間</span>
                </div>
                <div class="flex items-baseline">
                  <span class="font-bold text-[36px]">1</span>  
                  <span class="font-bold text^[20px]">ヶ月</span>
                </div>
              </div>
            </div>

            <div class="flex flex-col gap-[15px] leading-none">
              <div class="flex flex-col gap-[15px]">
                <div class="flex items-start">
                  <span class="font-medium text-[14px] text-[#333] w-[100px] shrink-0">サポート期間</span>
                  <span class="font-medium text-[16px]">卒業後無期限</span>
                </div>
                <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
              </div>

              <div class="flex flex-col gap-[15px]">
                <div class="flex items-start">
                  <span class="font-medium text-[14px] text-[#333] w-[100px] shrink-0">学べる内容</span>
                  <span class="font-medium text-[16px]">HTML/CSS、JavaScript、PHP、Vue.jsなど</span>
                </div>
                <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
              </div>

              <div class="flex items-start">
                <span class="font-medium text-[14px] text-[#333] w-[100px] shrink-0">サポート内容</span>
                <div class="flex flex-col gap-[15px] font-medium text-[16px]">
                  <span class="">案件獲得サポート</span>
                  <span class="">「びるどる」認定パートナーとして案件を優先紹介</span>
                  <span class="">サポートセンターで制作を全面サポート</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full md:w-[385px] shadow-[2px_2px_4px_0px__rgba(0,0,0,0.25)] shadow-[2px_2px_10px_0_rgba(0,0,0,0.1)] bg-white">
          <div class="w-full h-[10px] bg-gradient-to-r from-[#F35871] to-[#E03651]"></div>
          <div class="px-[15px] md:px-[30px] py-[35px] flex flex-col gap-[20px]">
            <div class="flex flex-col items-center">
              <div class="font-bold tracking-[0.05em] leading-none bg-gradient-to-b from-[#F35871] to-[#E03651] bg-clip-text text-transparent">
                <span class="text-[30px] md:text-[36px]">中期</span>
                <span class="text-[28px] md:text-[32px]">コース</span>
              </div>
            </div>

            <div class="px-[25px] md:px-[15px] py-[10px] md:py-[12px] bg-[#F6F6F6] flex items-center justify-between leading-none">
              <div class="flex items-center justify-center gap-[10px] md:gap-[20px]">
                <div class="px-[5px] py-[2px] bg-gradient-to-r from-[#E03651] to-[#F35871] shrink-0">
                  <span class="font-bold text-[14px] text-white">料金</span>
                </div>
                <div class="flex items-baseline gap-[2px] md:gap-[5px]">
                  <span class="font-bold text-[36px]">30</span>  
                  <span class="font-bold text-[20px]">万円</span>
                </div>
              </div>
              <div class="flex items-center gap-[10px] md:gap-[20px]">
                <div class="px-[5px] py-[2px] bg-gradient-to-r from-[#F35871] to-[#E03651] shrink-0">
                  <span class="font-bold text-[14px] text-white">学習期間</span>
                </div>
                <div class="flex items-baseline">
                  <span class="font-bold text-[36px]">3</span>  
                  <span class="font-bold text^[20px]">ヶ月</span>
                </div>
              </div>
            </div>

            <div class="flex flex-col gap-[15px] leading-none">
              <div class="flex flex-col gap-[15px]">
                <div class="flex items-start">
                  <span class="font-medium text-[14px] text-[#333] w-[100px] shrink-0">サポート期間</span>
                  <span class="font-medium text-[16px]">卒業後無期限</span>
                </div>
                <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
              </div>

              <div class="flex flex-col gap-[15px]">
                <div class="flex items-start">
                  <span class="font-medium text-[14px] text-[#333] w-[100px] shrink-0">学べる内容</span>
                  <span class="font-medium text-[16px]">HTML/CSS、JavaScript、PHP、Vue.jsなど</span>
                </div>
                <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
              </div>

              <div class="flex items-start">
                <span class="font-medium text-[14px] text-[#333] w-[100px] shrink-0">サポート内容</span>
                <div class="flex flex-col gap-[15px] font-medium text-[16px]">
                  <span class="">案件獲得サポート</span>
                  <span class="">「びるどる」認定パートナーとして案件を優先紹介</span>
                  <span class="">サポートセンターで制作を全面サポート</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full md:w-[385px] shadow-[2px_2px_4px_0px__rgba(0,0,0,0.25)] shadow-[2px_2px_10px_0_rgba(0,0,0,0.1)] bg-white">
          <div class="w-full h-[10px] bg-gradient-to-r from-[#F35871] to-[#E03651]"></div>
          <div class="px-[15px] md:px-[30px] py-[35px] flex flex-col gap-[20px]">
            <div class="flex flex-col items-center">
              <div class="font-bold tracking-[0.05em] leading-none bg-gradient-to-b from-[#F35871] to-[#E03651] bg-clip-text text-transparent">
                <span class="text-[30px] md:text-[36px]">長期</span>
                <span class="text-[28px] md:text-[32px]">コース</span>
              </div>
            </div>

            <div class="px-[25px] md:px-[15px] py-[10px] md:py-[12px] bg-[#F6F6F6] flex items-center justify-between leading-none">
              <div class="flex items-center justify-center gap-[10px] md:gap-[20px]">
                <div class="px-[5px] py-[2px] bg-gradient-to-r from-[#E03651] to-[#F35871] shrink-0">
                  <span class="font-bold text-[14px] text-white">料金</span>
                </div>
                <div class="flex items-baseline gap-[2px] md:gap-[5px]">
                  <span class="font-bold text-[36px]">50</span>  
                  <span class="font-bold text-[20px]">万円</span>
                </div>
              </div>
              <div class="flex items-center gap-[10px] md:gap-[20px]">
                <div class="px-[5px] py-[2px] bg-gradient-to-r from-[#F35871] to-[#E03651] shrink-0">
                  <span class="font-bold text-[14px] text-white">学習期間</span>
                </div>
                <div class="flex items-baseline">
                  <span class="font-bold text-[36px]">6</span>  
                  <span class="font-bold text^[20px]">ヶ月</span>
                </div>
              </div>
            </div>

            <div class="flex flex-col gap-[15px] leading-none">
              <div class="flex flex-col gap-[15px]">
                <div class="flex items-start">
                  <span class="font-medium text-[14px] text-[#333] w-[100px] shrink-0">サポート期間</span>
                  <span class="font-medium text-[16px]">卒業後無期限</span>
                </div>
                <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
              </div>

              <div class="flex flex-col gap-[15px]">
                <div class="flex items-start">
                  <span class="font-medium text-[14px] text-[#333] w-[100px] shrink-0">学べる内容</span>
                  <span class="font-medium text-[16px]">HTML/CSS、JavaScript、PHP、Vue.jsなど</span>
                </div>
                <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
              </div>

              <div class="flex items-start">
                <span class="font-medium text-[14px] text-[#333] w-[100px] shrink-0">サポート内容</span>
                <div class="flex flex-col gap-[15px] font-medium text-[16px]">
                  <span class="">案件獲得サポート</span>
                  <span class="">「びるどる」認定パートナーとして案件を優先紹介</span>
                  <span class="">サポートセンターで制作を全面サポート</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="hero-bg bg-cover bg-right bg-no-repeat gap-[40px] py-[100px] flex flex-col items-center">
      <div class="flex flex-col items-center gap-[10px]">
        <span class="font-bold text-[36px] leading-none tracking-[0.05em]">入校～卒業後の</span>
        <span class="font-bold text-[36px] md:text-[48px] leading-none tracking-[0.05em]">活躍イメージ</span>
      </div>
      <div class="flex flex-col gap-[10px] w-full px-[15px]">
        <div class="flex flex-col items-center">
          <div class="shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] flex">
            <div class="bg-linear-to-r from-brand-pink-dark to-brand-pink-light px-[20px] py-[30px] gap-[5px] font-bold leading-none tracking-[0em] flex flex-col md:flex-row items-center justify-center">
              <div class="flex flex-col items-center justify-center text-white">
                <span class="text-[12px]">STEP</span>
                <span class="text-[18px]">01</span>
              </div>
              <img src="./assets/icon.svg" />
            </div>
            <div class="md:w-[528px] md:h-[114px] p-[20px] gap-[5px] bg-white flex flex-col">
              <span class="font-bold text-[18px] md:text-[20px] leading-none tracking-[0.05em]">カウンセラー面談</span>
              <span class="font-medium text-[14px] md:text-[16px] leading-[1.2] tracking-[0em]">一人ひとりに合わせて、最適な学習プランとロードマップを組み立てていきます。</span>
            </div>
          </div>
          <img src="./assets/Polygon.svg" class="mt-[10px]"/>
        </div>

        <div class="flex flex-col items-center">
          <div class="shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] flex">
            <div class="bg-linear-to-r from-brand-pink-dark to-brand-pink-light px-[20px] py-[30px] gap-[5px] font-bold leading-none tracking-[0em] flex flex-col md:flex-row items-center justify-center">
              <div class="flex flex-col items-center justify-center text-white">
                <span class="text-[12px]">STEP</span>
                <span class="text-[18px]">02</span>
              </div>
              <img src="./assets/icon2.svg" />
            </div>
            <div class="md:w-[528px] md:h-[114px] p-[20px] gap-[5px] bg-white flex flex-col">
              <span class="font-bold text-[18px] md:text-[20px] leading-none tracking-[0.05em]">リアルタイム授業</span>
              <span class="font-medium text-[14px] md:text-[16px] leading-[1.2] tracking-[0em]">週1回2時間程度、プロの講師から直接講義を受けられます。
                テキストや教材では中々理解が難しいポイントをわかりやすく丁寧に解説します。</span>
            </div>
          </div>
          <img src="./assets/Polygon.svg" class="mt-[10px]"/>
        </div>
        
        <div class="flex flex-col items-center">
          <div class="shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] flex">
            <div class="bg-linear-to-r from-brand-pink-dark to-brand-pink-light px-[20px] py-[30px] gap-[5px] font-bold leading-none tracking-[0em] flex flex-col md:flex-row items-center justify-center">
              <div class="flex flex-col items-center justify-center text-white">
                <span class="text-[12px]">STEP</span>
                <span class="text-[18px]">03</span>
              </div>
              <img src="./assets/icon3.svg" />
            </div>
            <div class="md:w-[528px] md:h-[114px] p-[20px] gap-[5px] bg-white flex flex-col">
              <span class="font-bold text-[18px] md:text-[20px] leading-none tracking-[0.05em]">課題提出</span>
              <span class="font-medium text-[14px] md:text-[16px] leading-[1.2] tracking-[0em]">リアルタイム授業で習ったことをもとに、デザイン制作の課題を
                クリアにします。スキル習得期間はstep2とstep3を繰り返します。</span>
            </div>
          </div>
          <img src="./assets/Polygon.svg" class="mt-[10px]"/>
        </div>
        
        <div class="flex flex-col items-center">
          <div class="shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] flex">
            <div class="bg-linear-to-r from-brand-pink-dark to-brand-pink-light px-[20px] py-[30px] gap-[5px] font-bold leading-none tracking-[0em] flex flex-col md:flex-row items-center justify-center">
              <div class="flex flex-col items-center justify-center text-white">
                <span class="text-[12px]">STEP</span>
                <span class="text-[18px]">04</span>
              </div>
              <img src="./assets/icon4.svg" />
            </div>
            <div class="md:w-[528px] md:h-[114px] p-[20px] gap-[5px] bg-white flex flex-col">
              <span class="font-bold text-[18px] md:text-[20px] leading-none tracking-[0.05em]">卒業制作</span>
              <span class="font-medium text-[14px] md:text-[16px] leading-[1.2] tracking-[0em]">これまでに習ったことを活かしポートフォリオづくりを兼ねて卒業
                制作を行います。講師から合格判定をもらえたら、卒業が可能です。</span>
            </div>
          </div>
          <img src="./assets/Polygon.svg" class="mt-[10px]"/>
        </div>
        
        <div class="flex flex-col items-center">
          <div class="shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] flex">
            <div class="bg-linear-to-r from-brand-pink-dark to-brand-pink-light px-[20px] py-[30px] gap-[5px] font-bold leading-none tracking-[0em] flex flex-col md:flex-row items-center justify-center">
              <div class="flex flex-col items-center justify-center text-white">
                <span class="text-[12px]">STEP</span>
                <span class="text-[18px]">05</span>
              </div>
              <img src="./assets/icon5.svg" />
            </div>
            <div class="md:w-[528px] md:h-[114px] p-[20px] gap-[5px] bg-white flex flex-col">
              <span class="font-bold text-[18px] md:text-[20px] leading-none tracking-[0.05em]">認定バッジ獲得</span>
              <span class="font-medium text-[14px] md:text-[16px] leading-[1.2] tracking-[0em]">卒業後は「びるどる」の認定バッジを獲得でき、認定パートナーとして案件紹介を受けられます。</span>
            </div>
          </div>
          <img src="./assets/Polygon.svg" class="mt-[10px]"/>
        </div>
        
        <div class="flex flex-col items-center">
          <div class="shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] flex">
            <div class="bg-linear-to-r from-brand-pink-dark to-brand-pink-light px-[20px] py-[30px] gap-[5px] font-bold leading-none tracking-[0em] flex flex-col md:flex-row items-center justify-center">
              <div class="flex flex-col items-center justify-center text-white">
                <span class="text-[12px]">STEP</span>
                <span class="text-[18px]">06</span>
              </div>
              <img src="./assets/icon6.svg" />
            </div>
            <div class="md:w-[528px] md:h-[114px] p-[20px] gap-[5px] bg-white flex flex-col">
              <span class="font-bold text-[18px] md:text-[20px] leading-none tracking-[0.05em]">商談</span>
              <span class="font-medium text-[14px] md:text-[16px] leading-[1.2] tracking-[0em]">コンシェルジュの同席サポートのもと商談を行い、案件を実際に
                受注して報酬を受け取ることが可能です。</span>
            </div>
          </div>
          <img src="./assets/Polygon.svg" class="mt-[10px]"/>
        </div>
        
        <div class="flex flex-col items-center">
          <div class="shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] flex">
            <div class="bg-linear-to-r from-brand-pink-dark to-brand-pink-light px-[20px] py-[30px] gap-[5px] font-bold leading-none tracking-[0em] flex flex-col md:flex-row items-center justify-center">
              <div class="flex flex-col items-center justify-center text-white">
                <span class="text-[12px]">STEP</span>
                <span class="text-[18px]">07</span>
              </div>
              <img src="./assets/icon7.svg" />
            </div>
            <div class="md:w-[528px] md:h-[114px] p-[20px] gap-[5px] bg-white flex flex-col">
              <span class="font-bold text-[18px] md:text-[20px] leading-none tracking-[0.05em]">継続的な案件獲得</span>
              <span class="font-medium text-[14px] md:text-[16px] leading-[1.2] tracking-[0em]">ご自身のキャパシティと相談しながら、「びるどる」から紹介を
                受けた案件を受注し、実績と報酬を獲得していきます。</span>
            </div>
          </div>
          <img src="./assets/Polygon.svg" class="mt-[10px]"/>
        </div>
        
        <div class="flex flex-col items-center">
          <div class="shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] flex">
            <div class="bg-linear-to-r from-brand-pink-dark to-brand-pink-light px-[20px] py-[30px] gap-[5px] font-bold leading-none tracking-[0em] flex flex-col md:flex-row items-center justify-center">
              <div class="flex flex-col items-center justify-center text-white">
                <span class="text-[12px]">STEP</span>
                <span class="text-[18px]">08</span>
              </div>
              <img src="./assets/icon8.svg" />
            </div>
            <div class="md:w-[528px] md:h-[114px] p-[20px] gap-[5px] bg-white flex flex-col">
              <span class="font-bold text-[18px] md:text-[20px] leading-none tracking-[0.05em]">案件獲得の幅を広げる</span>
              <span class="font-medium text-[14px] md:text-[16px] leading-[1.2] tracking-[0em]">営業スキルを身につけると個人での受注や他のクラウドサービス
  からの案件受注も可能になります。
  ※専用の営業講座あり</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="chat-bg2 bg-cover bg-no-repeat bg-center w-full py-[70px] md:py-[100px] gap-[30px] md:gap-[40px] flex flex-col items-center relative">
      <div class="absolute inset-0 bg-black/70 z-0"></div>
      <div class="flex items-center gap-[20px] md:gap-[42px] text-medium leading-[1.4] relative z-10">
        <div class="bg-white  px-[20px] py-[17px] gap-[10px] flex flex-col items-center text-medium text-[14px] md:text-[16px] leading-[1.4] relative shadow-[2px_2px_0_0_rgba(0,0,0,0,0.25)]">
          <span class="">カリキュラムの</span>
          <span>詳細を知りたい！</span>
          <img src="./assets/vector.svg" class="absolute left-1/2 -translate-x-1/2 bottom-[-1px] translate-y-2.5" alt="" />
        </div>
        <div class="bg-white px-[20px] py-[17px] gap-[10px] flex flex-col items-center text-medium text-[14px] md:text-[16px] leading-[1.4] relative shadow-[2px_2px_0_0_rgba(0,0,0,0,0.25)]">
          <span class="">自分には</span>
          <span>どのコースが合ってる？</span>
          <img src="./assets/vector.svg" class="absolute left-1/2 -translate-x-1/2 bottom-[-1px] translate-y-2.5" alt="" />
        </div>
      </div>
      <div class="text-white gap-[7.41px] md:gap-[10px] flex flex-col items-center font-bold tracking-[0.05em] leading-none relative z-10">
        <span class="md:text-[36px] text-[30px]">無料相談では</span>
        <div class="flex flex-col md:flex-row items-center">
          <span class="md:text-[36px] text-[30px] leading-[1.2]">各コースのカリキュラム</span>
          <span class="md:text-[36px] text-[30px] leading-[1.2]">詳細もご案内！</span>
        </div>
        <div class="flex flex-col md:flex-row items-center">
          <span class="md:text-[20px] text-[16px] leading-[1.8]">気になる疑問/相談は全て</span>
          <span class="md:text-[20px] text-[16px] leading-[1.8]">プロのカウンセラーが即解消！</span>
        </div>
      </div>
      <div class="md:py-[30px] md:px-[60px] gap-[7.4px] md:gap-[10px] flex flex-col flex items-center relative z-10">
        <span class="text-[14.79px] md:text-[20px] text-white font-bold leading-none">＼ 最短30秒でかんたん予約！／</span>
        <button class="relative w-[286.24px] md:w-[387px] h-[53.25px] md:h-[72px] flex justify-center items-center py-[19.23px] md:py-[26px] px-[14.79px] md:px-[20px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light rounded-[3.7px] md:rounded-[5px] transition hover:brightness-110 shadow-[1.48px_1.48px_0_0_rgba(0,0,0,0.25)] md:shadow-[2px_2px_0_0_rgba(0,0,0,0.25)]">
          <span class="text-[17.75px] md:text-[24px] font-bold text-white tracking-[0.05em] leading-none shadow-[0px_0px_1.55px_0px_rgba(0,0,0,0.49)] md:shadow-[0_0_2.1px_0_rgba(0,0,0,0.49)]">無料相談に参加する</span>
          <Icon class="absolute text-[17.75px] md:text-[24px] font-bold text-white right-[10px] md:right-[15px]" icon="cuida:caret-right-outline"/>
        </button>
      </div>
    </section>
    
    <section class="flex flex-col items-center gap-[30px] md:gap-[40px] py-[70px] md:pt-[40px] md:pb-[80px] bg-[#FFF6F6]">

      <span class="font-bold text-[30px] md:text-[36px] leading-none tracking-[0.05em]">受講の流れ</span>

      <div class="gap-[10px] flex flex-col md:flex-row items-center w-full md:w-auto px-[30px]">
        <div class="flex flex-col md:flex-row items-center w-full">
          <div class="flex flex-col items-start w-full md:w-[310px] h-[289px] relative">
            <div class="w-full md:w-[310px] h-[4px] bg-gradient-to-r from-[#F35871] to-[#E03651] z-1"></div>
            <div class="flex w-[88px] h-[31px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light z-1 absolute top-[-15px] flex items-center justify-center [clip-path:polygon(0%_0%,90%_0%,100%_100%,0%_100%)]">
              <span class="font-bold text-[24px] tracking-[0em] leading-none text-white">01</span>
            </div>
            <div class="w-full md:w-[310px] h-[280px] gap-[16px] px-[15px] pt-[50px] pb-[30px] bg-white shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] absolute left-[0px] top-[0px] z-0 flex flex-col items-center justify-center">
              <img src="./assets/icon9.svg" />
              <div class="gap-[10px] flex flex-col items-center">
                <span class="font-bold text-[20px] leading-none tracking-[0.05em]">無料相談に参加</span>
                <div class="flex flex-col items-center font-medium text-[16px] leading-[1.5] tracking-[0.03em] ">
                  <span>無料相談に参加！</span>
                  <span>コチラから日程調整可能です！</span>
                </div>
              </div>
            </div>
          </div>
          <img src="./assets/Polygon.svg" class="md:-rotate-90" />
        </div>

        <div class="gap-[10px] flex flex-col md:flex-row items-center w-full">
          <div class="flex flex-col items-start w-full md:w-[310px] h-[289px] relative">
            <div class="w-full w-full md:w-[310px] h-[4px] bg-gradient-to-r from-[#F35871] to-[#E03651] z-1"></div>
            <div class="flex w-[88px] h-[31px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light z-1 absolute top-[-15px] flex items-center justify-center [clip-path:polygon(0%_0%,90%_0%,100%_100%,0%_100%)]">
              <span class="font-bold text-[24px] tracking-[0em] leading-none text-white">02</span>
            </div>
            <div class="w-full md:w-[310px] h-[280px] gap-[16px] px-[15px] pt-[50px] pb-[30px] bg-white shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] absolute left-[0px] top-[0px] z-0 flex flex-col items-center justify-center">
              <img src="./assets/icon10.svg" />
              <div class="gap-[10px] flex flex-col items-center">
                <span class="font-bold text-[20px] leading-none tracking-[0.05em]">受講申し込み</span>
                <div class="flex flex-col items-center font-medium text-[16px] leading-[1.5] tracking-[0.03em] ">
                  <span>お申し込みが確認でき次第、</span>
                  <span>担当者からご連絡させて</span>
                  <span>いただきます。</span>
                </div>
              </div>
            </div>
          </div>
          <img src="./assets/Polygon.svg" class="md:-rotate-90" />
        </div>

        <div class="flex flex-col items-start w-full md:w-[310px] h-[289px] relative">
          <div class="w-full md:w-[310px] h-[4px] bg-gradient-to-r from-[#F35871] to-[#E03651] z-1"></div>
          <div class="flex w-[88px] h-[31px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light z-1 absolute top-[-15px] flex items-center justify-center [clip-path:polygon(0%_0%,90%_0%,100%_100%,0%_100%)]">
            <span class="font-bold text-[24px] tracking-[0em] leading-none text-white">03</span>
          </div>
          <div class="w-full md:w-[310px] h-[280px] gap-[16px] px-[15px] pt-[50px] pb-[30px] bg-white shadow-[2px_2px_4px_0_rgba(0,0,0,0.25)] absolute left-[0px] top-[0px] z-0 flex flex-col items-center justify-center">
            <img src="./assets/icon11.svg" />
            <div class="gap-[10px] flex flex-col items-center">
              <span class="font-bold text-[20px] leading-none tracking-[0.05em]">受講開始</span>
              <div class="flex flex-col items-center font-medium text-[16px] leading-[1.5] tracking-[0.03em] ">
                <span>担当者がしっかりと</span>
                <span>サポートさせていただきます。</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="flex flex-col items-center px-[15px] py-[70px] md:py-[80px] gap-[30px] md:gap-[40px]">
      <span class="text-[30px] md:text-[36px] font-bold tracking-[0.05em] leading-none">よくある質問</span>
      <div class="flex flex-col gap-[30px]">
        <div class="gap-[10px] flex justify-left">
          <div class="w-[42px] h-[42px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light rounded-full text-white flex items-center justify-center">Q</div>
          <span class="font-bold text-[18px] leading-none tracking-[0.05em] mt-[10px]">ここにテキストが入ります。</span>
        </div>
        <div class="font-medium text-[16px] leading-[1.5] tracking=[0em] flex flex-col items-center justify-center">
          <span>ここにテキストが入ります。ここにテキストが入ります。ここにテキストが入ります。</span>
          <span>ここにテキストが入ります。ここにテキストが入ります。ここにテキストが入ります。</span>
        </div>
        <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
      </div>

      <div class="flex flex-col gap-[30px]">
        <div class="gap-[10px] flex justify-left">
          <div class="w-[42px] h-[42px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light rounded-full text-white flex items-center justify-center">Q</div>
          <span class="font-bold text-[18px] leading-none tracking-[0.05em] mt-[10px]">ここにテキストが入ります。</span>
        </div>
        <div class="font-medium text-[16px] leading-[1.5] tracking=[0em] flex flex-col items-center justify-center">
          <span>ここにテキストが入ります。ここにテキストが入ります。ここにテキストが入ります。</span>
          <span>ここにテキストが入ります。ここにテキストが入ります。ここにテキストが入ります。</span>
        </div>
        <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
      </div>

      <div class="flex flex-col gap-[30px]">
        <div class="gap-[10px] flex justify-left">
          <div class="w-[42px] h-[42px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light rounded-full text-white flex items-center justify-center">Q</div>
          <span class="font-bold text-[18px] leading-none tracking-[0.05em] mt-[10px]">ここにテキストが入ります。</span>
        </div>
        <div class="font-medium text-[16px] leading-[1.5] tracking=[0em] flex flex-col items-center justify-center">
          <span>ここにテキストが入ります。ここにテキストが入ります。ここにテキストが入ります。</span>
          <span>ここにテキストが入ります。ここにテキストが入ります。ここにテキストが入ります。</span>
        </div>
        <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
      </div>

      <div class="flex flex-col gap-[30px]">
        <div class="gap-[10px] flex justify-left">
          <div class="w-[42px] h-[42px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light rounded-full text-white flex items-center justify-center">Q</div>
          <span class="font-bold text-[18px] leading-none tracking-[0.05em] mt-[10px]">ここにテキストが入ります。</span>
        </div>
        <div class="font-medium text-[16px] leading-[1.5] tracking=[0em] flex flex-col items-center justify-center">
          <span>ここにテキストが入ります。ここにテキストが入ります。ここにテキストが入ります。</span>
          <span>ここにテキストが入ります。ここにテキストが入ります。ここにテキストが入ります。</span>
        </div>
        <div class="w-full border-t-[1px] border-dashed border-[#C3C3C3]"></div>
      </div>
    </section>

    <footer class="flex flex-col items-center justify-center py-[30px] gap-[17px] bg-linear-to-r from-brand-pink-dark to-brand-pink-light">
      <div class="flex items-center justify-center flex-wrap gap-[15px] md:gap-[30px] font-regular text-[11px] text-[14px] leading-none tracking-[0em] text-white">
        <span >特定商取引法に基づく表示</span>
        <span>運営者情報 </span>
        <span>プライバシーポリシー </span>
      </div>
      <span class="font-regular text-[16px] md:text-[20px] tracking-[0em] leading-none text-white">Copyright © 2025 びるどる. All rights reserved.</span>
    </footer>
  </div>
</template>
