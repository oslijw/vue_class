<template>
  <div class="log_show container">
    <br /><br /><br /><br />
    <h2 class="col-md-8 text-left"><b>From now on, share your life</b></h2><br /><br /><br /><br />
    <h5 class="text-right"><a href='/log_write'>Ready to write a log? Click here</a></h5>
    <br /><hr />
    <h3>What have I ever done?</h3><br />
    <table class="table">
      <tr v-for="item in log_list" :key="item.log_id">
        <Singlelogshow
          :log_id="item.log_id"
          :title="item.title"
          :author="item.author"
          :context="item.context"
          :date="item.date"
          :show='true'
        />
      </tr>
    </table>
    <!-- <Singlelogshow v-for="item in log_list" :key="item"></Singlelogshow> -->
  </div>
</template>

<script>
// @ is an alias to /src

import Singlelogshow from "@/components/Singlelogshow.vue";

export default {
  name: "log_show",
  data() {
    return {
      log_list: [
        {
          log_id: "1",
          title: "基于微博数据挖掘的“新冠疫情”评论文本分析",
          author: "岳宗朴;刘彩;李莹;陆文静",
          date: "品位经典. 2020年12期 ",
          context:
            '利用网络爬虫方法抓取微博评论,进行文本分析、文本语句中心词分析,绘制词云图,分析此次微博舆情状况及情感取向。认为"新冠疫情""新型冠状病毒""疫情通报""政策公告"以及"社会支持"的关注度较高。在本研究限制时间段内,网民对于"新冠肺炎疫情"稳定在以积极情绪为主导的态势。本次疫情政府信息公开透明,少有谣言滋生,为今后突发公共卫生事件应对提供一定经验。',
        },
        {
          log_id: "2",
          title: "基于Elasticsearch的京津冀水环境搜索引擎的设计与实现",
          author: "张会清;张乐",
          date: "自动化技术与应用. 2020年11期",
          context:
            "针对京津冀水环境信息资源出口不一、范围不同,且不能得到精确检索的问题,本文采用Elasticsearch分布式索引检索技术,将京津冀水环境数据资源进行融合共享,构建了京津冀水环境搜索引擎系统。该系统包括数据采集、数据索引、数据检索、界面展示四个模块。重点对搜索的评分机制做了改进并对检索内容进行重排序。通过实验表明,与通用搜索引擎以及传统数据库相比,所实现的搜索引擎系统可以更加准确、快速地实现用户的检索需求。",
        },
        {
          log_id: "2",
          title: "基于Elasticsearch的京津冀水环境搜索引擎的设计与实现",
          author: "张会清;张乐",
          date: "自动化技术与应用. 2020年11期",
          context:
            "针对京津冀水环境信息资源出口不一、范围不同,且不能得到精确检索的问题,本文采用Elasticsearch分布式索引检索技术,将京津冀水环境数据资源进行融合共享,构建了京津冀水环境搜索引擎系统。该系统包括数据采集、数据索引、数据检索、界面展示四个模块。重点对搜索的评分机制做了改进并对检索内容进行重排序。通过实验表明,与通用搜索引擎以及传统数据库相比,所实现的搜索引擎系统可以更加准确、快速地实现用户的检索需求。",
        },
        {
          log_id: "2",
          title: "基于Elasticsearch的京津冀水环境搜索引擎的设计与实现",
          author: "张会清;张乐",
          date: "自动化技术与应用. 2020年11期",
          context:
            "针对京津冀水环境信息资源出口不一、范围不同,且不能得到精确检索的问题,本文采用Elasticsearch分布式索引检索技术,将京津冀水环境数据资源进行融合共享,构建了京津冀水环境搜索引擎系统。该系统包括数据采集、数据索引、数据检索、界面展示四个模块。重点对搜索的评分机制做了改进并对检索内容进行重排序。通过实验表明,与通用搜索引擎以及传统数据库相比,所实现的搜索引擎系统可以更加准确、快速地实现用户的检索需求。",
        },
        {
          log_id: "2",
          title: "基于Elasticsearch的京津冀水环境搜索引擎的设计与实现",
          author: "张会清;张乐",
          date: "自动化技术与应用. 2020年11期",
          context:
            "针对京津冀水环境信息资源出口不一、范围不同,且不能得到精确检索的问题,本文采用Elasticsearch分布式索引检索技术,将京津冀水环境数据资源进行融合共享,构建了京津冀水环境搜索引擎系统。该系统包括数据采集、数据索引、数据检索、界面展示四个模块。重点对搜索的评分机制做了改进并对检索内容进行重排序。通过实验表明,与通用搜索引擎以及传统数据库相比,所实现的搜索引擎系统可以更加准确、快速地实现用户的检索需求。",
        },
        {
          log_id: "2",
          title: "基于Elasticsearch的京津冀水环境搜索引擎的设计与实现",
          author: "张会清;张乐",
          date: "自动化技术与应用. 2020年11期",
          context:
            "针对京津冀水环境信息资源出口不一、范围不同,且不能得到精确检索的问题,本文采用Elasticsearch分布式索引检索技术,将京津冀水环境数据资源进行融合共享,构建了京津冀水环境搜索引擎系统。该系统包括数据采集、数据索引、数据检索、界面展示四个模块。重点对搜索的评分机制做了改进并对检索内容进行重排序。通过实验表明,与通用搜索引擎以及传统数据库相比,所实现的搜索引擎系统可以更加准确、快速地实现用户的检索需求。",
        }
      ],
    };
  },
  components: {
    Singlelogshow,
  },
};
</script>
