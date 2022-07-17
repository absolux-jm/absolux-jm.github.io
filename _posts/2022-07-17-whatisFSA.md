---
layout: single
title: What is Automata?

categories: Automata
---

<script
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"
  type="text/javascript">
</script>

# What is Automata?
Automata(단수형: automaton)의 개념은 17세기 과학적 결정론에서 기원한다.
물리적 세계에 대한 정확한 이해가 늘어가면서 우주가 하나의 기계와 같이 보였으며, 이미 Descates (1596-1650) 때부터 동물의 행동이나 사람을 수학적으로 기술할 수 있다고 추측하였다.
그러나 수 세기 간 결정론과 개인의 자유 의지에 관한 격렬한 논쟁이 오갔음에도 컴퓨터에 한해서는 그러한 논쟁이 없었으며, 이를 이용한 기술법이 두뇌를 설명할 수 있는지 역시 확신할 수 없다.
허나 이러한 이론은 컴퓨터의 설계, 작동, 그리고 해당 접근법의 한계를 이해함에 도움이 된다.
가장 중요한 이론적 장치 중 하나로 Alan Turing (1912-1954)의 이름을 딴 Turing machine이 있다.
Turing machine의 이해를 위해서는 이의 기본형인 finite state automaton을 이해해야 하며, automaton으로도 축약되는 이 machine은 바로 Kleene의 1956년 논문에서 정의된다.
해당 정의가 나온 배경은 그의 이전 논문 'Representation of Events in Nerve Sets and Finite Automata' (1951)에 등장한다.
여하간 automaton은 매우 간단함에도 수학과 이론 전산학에서 중요한 결과를 이끌어내었다.

# Understanding Basics
Automata는 자판기를 생각하면 아주 간단하다.
이해의 편의상 5원, 10원, 20원 동전을 여러 개 가지고 있다고 가정하자.
커피 한 잔이 20원이라면, 이를 뽑기 위해 돈을 순서대로 지불하는 방법은 다음처럼 나타낼 수 있다:

$$ (20), (10, 10), (10, 5, 5), (5, 10, 5), (5, 5, 10), (5, 5, 5, 5). $$

이제 machine이 $$q_{0}, q_{5}, q_{10}, q_{15}, q_{20}$$의 다섯 개의 states를 가진다고 생각하자.
각 첨자는 자판기가 받은 동의 총량을 의미한다.
$$q_0$$는 돈을 지불하기 시작하는 상태이므로 initial state라 하고, 커피 한 잔을 제공하는 기준인 20원을 모두 수령하면 $q_{20}$ state가 되며 이를 terminal state라 한다.
이를 가중치를 둔 유향 그래프로 표시할 수 있으며, finite state automaton의 전신형은 수학적으로 표기될 뿐, 사실상 이와 다르지 않다.
