#  UBET 幸运之门
 
    ubet是基于eos的智能游戏合约，不依赖中心化服务器，数据全部上链，所以我们不用设计前端，真正实现公平公开的游戏。
    秉承去中心化原则，后期代码会全部开源，团队会放弃合约权限，移交至黑洞地址
    目前处于早鸟运营期，越早加入可获取更多权证UBET。
    
# 游戏玩法：  
    1、规则：每局100张幸运卡，每张幸运卡需要1个EOS购买。系统会有一定概率在每次用户购买时进行空投。
            每一局幸运卡会产生三个幸运号码，分别作为一等奖，二等奖和三等奖。
            同时空投等比例UBET，每名用户当天购买后可以进行一次签到，获取一定量的UBET。
            同时游戏进行时会随机进行UBET代币空投，每张幸运卡的卖出，空投概率提高3%。
            游戏设置了玩家关系网，空投的UBET会有10%的比例作为对推荐人进行奖励
            
    2、购买：直接向ubetubetubet合约转账，每次购买转账必须为整数个EOS，
            同时每次操作间隔5s才能进行下一次购买，不符合规则的转账都会被视为参与失败，每局游戏自动开始，结束，清算。
            间隔5s才能进行下一次购买,购买成功后，可以查询到本局你持有的幸运卡号。
    3、开奖：当一局的100张幸运卡售完时，合约会根据当前时间等使用xoroshiro128算法产生随机数，
            产生头奖、二等奖和三等奖三个幸运卡，将分别获得奖池的50%、30%、20%作为游戏奖励，
            同时会将总奖池的10%注入到权益池，为持有FP代币的玩家进行分红。
            目前每局游戏数据需要消耗2kb内存。(如果游戏成为爆款，内存将被持续购买，各位的ram解套有望！)

    说明：UBET权证总量10000000个，将全部分发给社区参与者，团队不会持有份额。
         游戏每局盘子较小，玩家的投入和收益将迅速体现，同时也将获取大量的UBET权益，游戏既挖矿。
         同时游戏中机器人将无利可图而不会破坏公平规则。本游戏开发初心是为了依托区块链，建立真正公平公开的规则。
         也是为了刺激EOS ram市场的活力！
         如果说数字货币是炒作，那么团队将致力于用区块链技术让世界变得公平。本游戏是团队的小试牛刀，更多游戏敬请期待！

## 安装
  #### 前端：
       提前安装好node.js环境，进入到ubet目录下，npm run build，将打包的dist目录拷贝至服务器，用nginx做反向代理，即可对外提供服务
  #### 合约：
       合约以及合约部署脚本在ubet/deploy目录下，必须将脚本中的私钥和公钥为测试网络账号，必须修改为你自己的私钥和公钥
       * 创建团队账号ubetubetfee1,用于接收游戏手续费，团队账号ubetubetdev1为默认玩家推荐账号。
       * 创建部署发币账号fairubetubet，运行deployTokenContract.js，将eosio.token合约部署，运行issueToken.js，发行游戏币UBET。
       * 创建部署游戏合约账号ubetubetubet，运行deployContract.js，将游戏合约bet部署至该账号，继续运行updateAuth.js，更新合约的权限。
 
                                                                                          
本游戏开源仅用于个人进行测试网络研究区块链技术，推动社会向着更好的方向发展，如果有用于商业用途，产生的任何事故纠纷均与本项目无关。
如果你喜欢EOS，并觉得本项目对你的认识有帮助，那么请喝个咖啡吧！

