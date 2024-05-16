---
layout: post
title: "Unreal에서 Pawn이 바라보는 방향(Pawn의 Rotation)을 얻는 방법."
description: "A graphic designer is a professional within the graphic design and graphic arts industry."
date: 2024-05-15
feature_image: images/UnrealLogo.jpg
tags: [Tips, Unreal engine]
---

내가 바라보는 방향으로 투사체를 발사하고 싶다고 할 때 Get Actor Rotation에 player pawn을 집어 넣어 바라보는 방향을 알 수 있을거라고 생각할 수 있다.

<!--more-->

그러나 이런 방식으로 pawn의 rotation을 얻으면 내가 바라보는 방향으로 투사체가 발사되지 않는다는 것을 알 수 있다.   

## 보는 방향이 바뀐다고 해서 Pawn의 Roation이 바뀌는 것이 아니다.
게임을 시작한 직후의 Pawn의 Transform이 다음과 같다고 하자.
![alt text](UnrealPawnRotation1.jpg)   

그리고 마우스를 움직여 Pawn이 다른 방향을 바라보게 만든 다음 다시 Transform을 보자. Rotation에 변화가 있었을까?
![alt text](UnrealPawnRotation1-2.jpg)   

그렇다. **Pawn의 바라보는 방향이 바뀌어도 Pawn의 Rotation이 바뀌는 것은 아니다.**

그렇다면 어떻게 Pawn이 바라보는 방향을 나타내는 rotation을 얻을 수 있을까?

## Control Rotation
Player가 바라보는 Orientation을 위한 Rotation을 알기 위해서는 **Control Rotation을 이용**해야 한다. 
Control Rotation에 우리가 원하는 pawn이 바라보는 방향을 위한 rotation이 적혀 있다. 