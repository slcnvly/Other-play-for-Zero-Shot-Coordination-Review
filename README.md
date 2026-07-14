# **Other-play-for-Zero-Shot-Coordination-Review**
Review of "Other-play" for Zero-Shot Coordination with Questions, Issues

This repository documents my research process of reading Other-Play for Zero-Shot Coordination, implementing its core ideas, and examining the assumptions and limitations of the paper.

The goal is not merely to summarize the paper or reproduce its official implementation. Instead, I aim to understand the problem addressed by the paper precisely, investigate how the proposed method works through direct implementation in small environments, and identify phenomena that are not fully explained by the existing analysis or potential new research questions that emerge during this process. 

## 1. One Sentence Summary
This paper proposes Other-Play, a symmetry-based training method for zero-shot coordination, to prevent agents from relying on arbitrary conventions learned through self-play, and shows that it improves cross-play performance between independently trained agents and achieves stronger coordination with human partners in Hanabi.  
필자의 이해를 위해 여기부터 한국어로 작성하겠음,,

## 2. Research Problem 
- **이 논문이 해결하려는 문제는 무엇인가?**<br>
  이 논문은 에이전트가 학습 과정에서 한 번도 만나지 않은 새로운 파트너와 추가 학습이나 사전 합의 없이 바로 협력해야 하는 zero-shot coordination 문제를 다룬다.

- **왜 이 문제가 중요한가?**<br>
  실제 multi-agent 환경에서는 하나의 에이전트가 앞으로 만날 모든 파트너와 미리 함께 학습할 수 없다. 독립적으로 개발된 다른 agent나 인간 사용자와 처음 만난 상황에서도 즉시 협력해야하는 상황에선 특정 학습 파트너와만 높은 성능을 내는 것으로는 충분하지 않다.

- **기존 방식으로는 왜 해결되지 않는가?**<br>
  기존 marl 방식인 self-play는 agent가 다중 agent들과 함께 반복적으로 게임하면서, 함께 높은 보상(공동 return 최대화)을 얻는 전략을 만든다.
그러나 이렇게 co-trained된 multi-agent는 서로에게만 통하는 특수한 '관습' 내지는 '약속'을 만들어낼 수 있으며, 이는 새로운 파트너, agent에겐 통하지 않을 수 있다.

## 3. Existing Approaches and Gap 
- **기존 방법은 무엇인가?**<br>


- 각각 어떤 가정을 하는가? - 저자들이 주장하는 핵심 한계는 무엇인가? 




# 4\. Main Contributions # 5\. Method ## 5.1 Input / State / Observation ## 5.2 Model Architecture ## 5.3 Objective / Loss Function ## 5.4 Training Procedure ## 5.5 Inference Procedure # 6\. Experiments - Environment / Dataset: - Baselines: - Metrics: - Main result: - Ablation: - Generalization test: # 7\. Assumptions - 이 방법이 성립하려면 무엇을 가정하는가? - 현실적인 가정인가? # 8\. Strengths # 9\. Weaknesses / Limitations # 10\. Questions - 이해하지 못한 개념: - 논리적으로 의심되는 부분: - 추가로 확인할 실험: # 11\. Connections - 어떤 기존 논문과 연결되는가? - 내가 공부한 개념과 어떤 관계인가? # 12\. Research Ideas - 이 방법을 어떻게 확장할 수 있는가? - 가정을 완화할 수 있는가? - 다른 환경에 적용할 수 있는가? - 실패 사례를 개선할 수 있는가? # 13\. Final Evaluation - 중요도: 1–5 - 재독 필요 여부: - 내 연구와의 관련성:
