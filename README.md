# **Other-play-for-Zero-Shot-Coordination-Review**
Review of "Other-play" for Zero-Shot Coordination with Questions, Issues

This repository documents my research process of reading Other-Play for Zero-Shot Coordination, implementing its core ideas, and examining the assumptions and limitations of the paper.

The goal is not merely to summarize the paper or reproduce its official implementation. Instead, I aim to understand the problem addressed by the paper precisely, investigate how the proposed method works through direct implementation in small environments, and identify phenomena that are not fully explained by the existing analysis or potential new research questions that emerge during this process. 

## 1. One Sentence Summary
This paper proposes Other-Play, a symmetry-based training method for zero-shot coordination, to prevent agents from relying on arbitrary conventions learned through self-play, and shows that it improves cross-play performance between independently trained agents and achieves stronger coordination with human partners in Hanabi.  
필자의 이해를 위해 여기부터 한국어로 작성하겠음,,

## 2. Research Problem 
- **이 논문이 해결하려는 문제는 무엇인가?**
  이 논문은 에이전트가 학습 과정에서 한 번도 만나지 않은 새로운 파트너와 추가 학습이나 사전 합의 없이 바로 협력해야 하는 zero-shot coordination 문제를 다룬다.

- **왜 이 문제가 중요한가?**
  실제 multi-agent 환경에서는 하나의 에이전트가 앞으로 만날 모든 파트너와 미리 함께 학습할 수 없다. 독립적으로 개발된 다른 agent나 인간 사용자와 처음 만난 상황에서도 즉시 협력해야하는 상황에선 특정 학습 파트너와만 높은 성능을 내는 것으로는 충분하지 않다.

- **기존 방식으로는 왜 해결되지 않는가?**
  기존 marl 방식인 self-play는 agent가 다중 agent들과 함께 반복적으로 게임하면서, 함께 높은 보상(공동 return 최대화)을 얻는 전략을 만든다.
그러나 이렇게 co-trained된 multi-agent는 서로에게만 통하는 특수한 '관습' 내지는 '약속'을 만들어낼 수 있으며, 이는 새로운 파트너, agent에겐 통하지 않을 수 있다.
