<template>
  <el-container direction="vertical">
    <myheader index="/achievements"></myheader>
    <el-main class="main-content">

      <el-row :gutter="0" type="flex" justify="center">
        <el-col :xs="20" :sm="18" :md="16" :lg="14" :xl="12">
          <h1>发表论文</h1>

          <ul>
            <li v-for="item in papers" class="item animated zoomIn">
              {{item}}
            </li>
          </ul>

          <el-divider><i class="el-icon-notebook-2"></i></el-divider>


<!--          <h1>申请专利</h1>-->

<!--          <ul>-->
<!--            <li v-for="item in patents" class="item">-->
<!--              {{item}}-->
<!--            </li>-->
<!--          </ul>-->

<!--          <el-divider><i class="el-icon-copy-document"></i></el-divider>-->

          <h1>获得奖项</h1>

          <ul>
            <li v-for="item in awards" class="item">
              {{item}}
            </li>
          </ul>
        </el-col>
      </el-row>
    </el-main>


    <myfooter></myfooter>
  </el-container>
</template>
<script>
  import myheader from '~/components/myheader.vue'
  import myfooter from '~/components/myfooter.vue'

  export default {
    name: "achievements",
    data() {
      return {
        papers: [
          'Qianwei Zhuang, Yuan Liu Lisi Chen, Zhengpeng Ai. Proof of Reputation: A Reputation-based Consensus Protocol for Blockchain based Systems, 2019 International Electronics Communication Conference (IECC), 2019. EI',
          'Tianzhi Yang, Yuan Liu. A Smart Agent based Blockchain Applicaiton Architecture, The 4th International Conference on Crowd Science and Engineering(ICCSE), 2019. EI ',
          'Shuai Sun, Yuan Liu, Xingren Chen, Guibing Guo. The 17th IEEE International Symposium on Parallel and Distributed Processing with Applications(ISPA) 2019.CCF C类',
          'Zheng Zhao, Yuan Liu. A Blockchain based Identity Management System Considering Reputation, 2nd IEEE International Conference on Computer Systems, Electronics and Control(ICCSEC), 2018.EI ',
          'Jin Bai, Yuan Liu. A Reputation Model Considering Buyer Subjectivity and Product Return Behavior, 2nd IEEE International Conference on Computer Systems, Electronics and Control(ICCSEC), 2018. EI',
          'Guibing Guo, Tianzhi Yang, Yuan Liu, Search Engine Based Proper Privacy Protection Scheme. IEEE Access 6: 78551-78558,2018. SCI 1区',
          'Yuan Liu, Jie Zhang, Quanyan Zhu, Xingwei Wang. CONGRESS: A Hybrid Reputation System for Coping with Rating Subjectivity, IEEE Transactions on Computational Social Systems, 2017. EI',
          'Yuan Liu, Zheng Zhao, Guibing Guo, Xingwei Wang, Shuang Wang. An Identity Management System Based on Blockchain, 15th Annual Conference on Privacy, Security and Trust (PST), 2017.EI',
          'Yuan Liu, Usman Shittu Chidawa, Guibing Guo, Xingwei Wang, Shuang Wang. A Reputation Model for Aggregating Ratings based on Beta Distribution Function. 2nd International Conference on Crowd Science and Engineering (ICCSE), 2017.EI',
          'Yuan Liu, Jin Bai, Guibing Guo, Xingwei Wang, Zhenhua Tan. A Reputation Model Considering Repurchase Behavior and Mechanism Design to Promote Repurchase. The 10th International Conference on Security, Privacy and Anonymity in Computation, Communication and Storage (SpaCCS), 2017.EI',
          'Ning Luo, Huaxun Deng, Linfeng Zhao, Yuan Liu, Xingwei Wang, Zhenhua Tan. Multi-aspect Feature based Neural Network Model in Detecting Fake Reviews. 4th International Conference on Information Science and Control Engineering (ICISCE), 2017.EI',
          'Huaxun Deng, Lingfeng Zhao, Ning Luo, Yuan Liu, Xingwei Wang, Zhenhua Tan, Shuang Wang, and Fucai Zhou. Semi-supervised Learning based Fake Review Detection. IEEE International Symposium on Parallel and Distributed Processing with Applications (ISPA), 2017.EI',
          'Zhenhua Tan, Jingyu Ning, Yuan Liu, Xingwei Wang, Guangming Yang, Wei Yang. ECRModel: an Elastic Collusion-based Rumor-Propagation Model in Online Social Networks, IEEE Access, 2016. SCI 一区',
          'Yuan Liu, Chunyan Miao. A Survey of Incentives and Mechanism Design for Human Computation Systems, CoRR abs/1602.03277, 2016.',
          'Qiong Wu, Siyuan Liu, Chunyan Miao, Yuan Liu, Cyril Leung. A Social Curiosity Inspired Recommendation Model to Improve Precision, Coverage and Diversity. In Proceedings of the 2016 IEEE/WIC/ACM International Conference on Web Intelligence (WI), 2016.EI',
          'Zhenhua Tan, Yicong Niu, Yuan Liu, and Guangming Yang. A Novel Trust Model Based on SLA and Behavior Evaluation for Clouds. In Proceedings of the 2016 Annual Privacy, Security and Trust Conference (PST) 2016 EI',
          'Yuan Liu, Jie Zhang, Bo An, Sandip Sen. A simulation framework for measuring robustness of incentive mechanisms and its implementation in reputation systems, Journal of Autonomous Agents and Multi-agent Systems (JAAMAS), 2015.CCF B类',
          'Siyuan Liu, Chunyan Miao, Yuan Liu, Hui Fang, Han Yu, Jie Zhang, Yueting Chai, Cyril Leung: A Reputation Revision Mechanism to Mitigate the Negative Effects of Misreported Ratings. ICEC 2015: 7:1-7:8 EI',
          'Siyuan Liu, Chunyan Miao, Yuan Liu, Han Yu, Jie Zhang, Cyril Leung, An Incentive Mechanism to Elicit Truthful Opinions for Crowdsourced Multiple Choice Consensus Tasks. WI-IAT (2) 2015: 96-103 EI',
          'Yuan Liu “Towards the Design of Robust Incentive Mechanisms to Address Subjectivity and Dishonesty Problems in Agent Reporting”, PhD Thesis ',
          'Yuan Liu, Jie Zhang, Han Yu, and Chunyan Miao “ Reputation-aware Continuous Double Auction ”, in proceedings of 28th International Conference AAAI Conference on Artificial Intelligence, Student Poster Program, 2014 CCF A类',
          'Yuan Liu, Siyuan Liu, Hui Fang, Jie Zhang, Han Yu, and Chunyan Miao “ RepRev: Mitigating the Negative Effects of Misreported Ratings ”, in proceedings of 28th International Conference AAAI Conference on Artificial Intelligence, Student Poster Program, 2014 CCF A类',
          'Yuan Liu, Jie Zhang, An Bo, and Sandip Sen “ A Practical Robustnesss Measure of Incentive Mechanisms ”, in proceedings of 13th International Conference on Autonomous Agents and Multiagent Systems (AAMAS), 2014 CCF B类 ',
          'Zeinab Noorian, Mohsen Mohkami, Yuan Liu, Hui Fang, Julita Vassileva, and Jie Zhang. SocialTrust: Adaptive Trust Oriented Incentive Mechanism for Social Commerce. In Proceedings of the 2014 IEEE/WIC/ACM International Conference on Web Intelligence, 2014 EI',
          'Yuan Liu, Jie Zhang “An incentive mechanism designed for e-marketplaces with limited inventory”, Electronic Commerce Research and Applications, 2013. SCI 二区',
          'Zeinab Noorian, Jie Zhang, Yuan Liu, Stephen Marsh, and Michael Fleming “ Trust-Oriented Buyer Strategies for Seller Reporting and Selection in Competitive Electronic Marketplaces ”, Journal of Autonomous Agents and Multi-Agent Systems (JAAMAS), 2013. CCF B类',
          'Yuan Liu “Towards the Design of a Robust Incentive Mechanism for E-Marketplaces with Limited Inventory”, in International Joint Conference on Autonomous Agents and Multiagent Systems (AAMAS), Doctorial Consortium, 2013, pages 1441-1442. CCF B类 ',
          'Yuan Liu, Jie Zhang “Robustness Evaluation of Incentive Mechanisms”, in International Joint Conference on Autonomous Agents and Multiagent Systems (AAMAS), 2013 (short paper), pages 1293-1294. CCF B类',
          'Yuan Liu, Qin Li, Jie Zhang “Coalition Formation Game based Reputation System”, in ACM EC Workshop on Incentives and Trust in E-Commerce (WIT-EC2012). EI ',
          'Yuan Liu, Jie Zhang, Qin Li “Design of an Incentive Mechanism to Promote Honesty in E-marketplaces with Limited Inventory”, in the proceedings of 14th Annual International Conference on Electronic Commerce, Singapore (ICEC2012), pages 54-61. EI',
          'Yuan Liu, Jie Zhang, Qin Li “An Incentive Mechanism to Promote Honesty in E-marketplaces with Limited Inventory ”, in the proceedings of 6th IFIP WG 11.11 International Conference on Trust Management, Surat, India (IFIPTM2012), pages 209-216. EI',
          'Yuan Liu, Jie Zhang, Quanyan Zhu “Design of a Reputation System based on Dynamic Coalition Formation”, in the proceedings of Third International Conference on Social Informatics, Singapore (SocInfo2011), pages 135-144. EI',

        ],
        patents: [
          '一种......算法',
          '基于......的模型',
          '基于......的系统'
        ],
        awards: [
          '全国大学生信息安全竞赛特等奖',
          'ACM程序设计大赛金奖'
        ]
      }
    },
    components: {
      myheader,
      myfooter
    }
  }
</script>

<style scoped>

  .item {
    margin: 10px 0;
  }


  li {
    color: #606266;
    text-align: justify;
    text-justify: inter-ideograph
  }


</style>


