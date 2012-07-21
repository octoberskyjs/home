
Nodeconf 2012 Day02 Sessions wrap-ujp
====================================

> 참고로, 본 페이지에는 아~주 일부분의 내용만 담겨 있습니다. 기타 자세한 내용은 한국에서의 랩업 세미나를 기대해 주세요. :)

사진링크: [day 2](https://picasaweb.google.com/107279487440516858381/Nodeconf_portland_day02) 

Porting node, Tim Caswell
---

- Spec을 만들고 구현하는 것이 중요한 것 같다.
- fiber를 좀 봐야 겠다.
- LUA coroutine 좋은것 같다.
- node 하려면 역시 C를 해야 하나 보다.
- 매우 인상적이었다. V8대신 LuaJit을 선택해 볼만 하겠다.
- node.js 모듈을 구현해 나가기 위해 구현해 나가는 방식이 재밌었다.
- two way
    - using C
    - using FFI(Fast Function Interface)

[slides & resources](https://github.com/creationix/nodeconf2012/)

Node Streams, Marco 
---
- Stream 시리즈 좋다!
- nFORGE개발하면서 겪은 문제랑 해결방법이, Marco의 문제랑 해결방법이랑 같아서 왠지 기분이 좋았다. 
- Stream 효율적이긴 한데 문제가 생겼을 때 처리가 어렵다.

[slides & resources](https://github.com/polotek/nodeconf-2012-streams-talk)

fast binary stream parsing - node-mysql, Felix Geisendörfer
---

- 2.0 쓰게 된 것
- protocal implementation을 해야 하는군.
- buffer[offset++] style 괜찮네...
- comma(,) first에 대한 사람들의 다른 반응들..
    - 이 스타리일 싫어하는 사람도 많구나!
- 예상밖으로 매우 재밌던 세션! 친절하고 재밌는 독일 아저씨였음

streams are userful when.., Max Ogden
---

- substack 비슷한 스피커
- webrtc가 스펙이 있었구나
- domnode 한번 봐야겠다 (오늘은 한번 봐야겠다가 참 많다)

[slides & resources](https://github.com/polotek/nodeconf-2012-streams-talk)

Streams at Scale, Matt Ranney
---

- 발표자료에 내용이 별로 없어서 힘들다. (영어 리스닝 잘 안되는데)
- redis로도 해결이 안된다.
- concurrency 문제는 접속 제한으로?
- 근데 뭐든 딱히 해결책은 안된다. (뭘 말하려는걸까)
- 음... 많이 해봤구나. 힘든 경험을 했구나
- scale 문제를 해결하려면 node internal을 봐라. 물론 어렵다.

dtrace
---

- dtrace를 보여줄 것 같더니만 끝나네
- 솔라리스하고 맥만 된다. 리눅스가 아직 안된다는게 슬프다.
- 엄청 좋다함

DTrace, Node.js, Flame Graphs, Dave Pacheco
---

- 플레임 그래프 언제봐도 인상적
- restify
- dtract는 궁극의 무기같지만 로우레벨이라 쓰기가 좀

[slides](http://dtrace.org/blogs/dap/files/2012/07/nodeconf.pdf)

So, you've got a memory leak, Danny Coates
---

- v8-profiler의 snapshot 찍는 기능이 인상적
- 처음이라 떠는구나
- v8-profiler의 데모는 좋을 뻔 했는데 좀 엉성하게 지나가버려서 아쉬움 

node-memwatch
---

- 메모리릭 해결은 재시작이 최고
- leak 발생시 emit하는게 잘 만들어져 있는 것 같음
- 메모리 heapsize가 계속 증가하면 leak 이벤트 발생
- heap diff 를 얻을 수 있다고 하는데 이게 언제와 언제의 차이인건지?
     - leak 이벤트와 leak 이벤트 사이
- 미래에 leak을 유발한 object의 정보까지 제공해주겠다고 한게 대단해보임

[links](https://github.com/lloyd/node-memwatch)

하드웨어 세션들
--------------

- Node JS & Black Box, Emily Rose

[slides](https://docs.google.com/presentation/d/1m1MiyNffoqeYQMLrtqnY990kJdfaPKhtyEXh5MQ6rC0/edit#slide=id.g14c70e36_0_0)


- Node-spi

[slides](https://www.dropbox.com/s/ff2k39ul5bs29e2/Node%20and%20SPI%20%28nodeconf2012%29.pdf)

- Johnny-Five

[slides](https://dl.dropbox.com/u/3531958/nodeconf/index.html#/)

- How I use node to communicate with hardware, Elijah Insua

[slides](http://tmpvar.com/nodeconf-2012/assets/fallback/index.html)

- 하드웨어는 그닥 관심이 없어서 아 그런가보다 하고 들었음
- 그러나 코드가 현실세계에서 (유용하게) 동작하는 모습은 매력적

최종정리
--------

- 사전에 준비를 하고 매일 저녁 정리하거나 하는 모습이 참 좋은 것 같다.
- 좀 충격이었다. 형식없고 정리안되어있고 가족적이고 축제같고. 부럽기도 하고. 내용은 둘째치고 그런 풍토를. voice박스에서 노래 못 불러서 아쉬움. 진행이 좀 미숙한 건 아쉬운 점. 미리 프로그램을 알 수 있었으면 좋았을걸
- 대단하다. 한국에서는 재현하기 어려운 컨퍼런스 분위기. 스텝의 참여가 좋다. 청중이 좋다. 반응 분위기 좋다.
- 한국은 뭐하나 보자, 잘하나 보자 하는 식으로 참가자가 참여가 잘 안한다. 바람잡이 심어야 하나?
- 숙제 한 가득 가지고 간다.
- 매우 유익했다.
- 프로그램 안 알려줘서 아쉽다.
- 한국에서도 노드컨프 아시아 같은 행사를 만들어야 겠다
- 내용이 정말 좋았던 것 같다. 거의 탑 수준. 왜 그런가 생각해봤는데 일단 관심있는 주제들이고 그 방면에 경험있는 사람들이 얘기해주고 (실제로 해본 사람들이) 굉장히 몰입할 수 있어서 컨퍼런스 수준이 내용면에서 굉장히 좋았다. 진행은 꽝. 아 700달러. 돌아가면 할 숙제가 많다. wrap-up을 같이 할 수 있어서 정말 좋았다. 이런 wrap-up을 빨리 하는게 훨씬 좋다(경험상). 같이 참여해주셔서 감사.
- 너무 오고 싶었던 컨퍼런스여서 오니 좋다. 그냥 있다는 것 만으로도 진행이 어쨌든 그냥 막 좋다. node와는 특별한 연이 있는 것도 있고. node가 좀 미숙한 감도 있는데 그것도 매력. 독일에서 컨퍼런스 하는거봤는데 열악한 환경에서 잘 하더라. 그거보니까 별거 아니란 생각이 들고 여기도 딱히 세련된 것은 없고. 내용은 집에서 동영상봐도 되지만 현지의 분위기를 느끼고 해외개발자들과 어울리는 것이 좋다. 혼자 있으면 와서 밥먹자고 데려가고 그럼. 하나도 못 알아들어도 이렇게 좋은데 다 알아들으면 얼마나 좋을까. 영어공부를 해서 다시 와야겠다. (nodeconf가 아니라도) 돈은 좀 많이 들었지만 오길 잘했다.

