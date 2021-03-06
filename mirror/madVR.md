## Contents

    

1. 소개 
2. 특징 

[[edit](http://rigvedawiki.net/r1/wiki.php/madVR?action=edit&section=1)]

## 1. 소개 ¶

[Doom9 포럼의 공식 스레드](http://forum.doom9.org/showthread.php?t=146228)

  

madshi Video Renderer. 동영상을 재생할 때 화면을 왜곡하거나 화질에 해를 끼치는 그래픽카드 자체의 로직은
차단(bypass)하고, 동시에 그래픽카드의 물리적인 성능은 최대한 활용해서, 화질에 이로운 고품질의 후처리를 통해 영상이 원래 의도한
화면을 최대한 더 좋은 화질로 보여주기 위해 탄생한 비디오 렌더러이다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/madVR?action=edit&section=2)]

## 2. 특징 ¶

목적이 목적인 만큼, 당연히 madVR을 통해서 나온 동영상의 화면은 매우 좋다.  
madVR은 8bit, 10bit, 16bit 영상 정보를 모두 입력받을 수 있고, 동영상 제작 시에 거의 필수적으로 압축하게 되는 색상
정보를 항상 업스케일링하며, 모든 작업을 16bit 공간에서 처리한다. 즉, 동영상을 실제 화면에 그려내는 렌더러의 역할에 있어서 최고의
방식으로 작동하며, 그래서 당연하게도 최고의 품질을 보여준다.

  

**하지만 현재 블루레이로 나오는 영상들은 기본 품질이 매우 뛰어나기 때문에 madVR를 쓰나 안 쓰나 인간의 눈으로 구별 가능한 부분이 거의 없다**라고 성급하게 일반화하는 것은 무리가 있다. 영상을 조금만 주의깊게 관찰한다면 흔히 '블루레이 급'이라고 일컫는 1080p HD 수준의 영상에서도 이미지 디테일이 달라지는 것을 확인할 수 있다. 또한 madVR을 설정하면서 필연적으로 조정하게되는 색공간을 올바르게 맞춰주는 작업만으로도 색상 경계가 타 영역으로 침범하는 버그 수준의 출력을 바로잡고 색상을 포함한 이미지의 경계가 살아나는 것을 볼 수 있다. 이러한 '이미지'에 대한 개선 뿐만 아니라, 영상의 떨림(Motion judder)을 걷어내는 기능을 통해 영상의 '움직임' 또한 개선된다. 동영상은 정지된 사진이 아니라 움직이는 영상이기 때문에 madVR의 이러한 '움직임' 개선 기능은 매우 중요하며 좋은 결과물을 보여준다. 사람의 눈과 귀는 더 좋은 것에 더 많이 더 자주 노출될 수록 그 감각이 향상된다. 아직 구분이 되지 않는다면 더 좋은 것에 좀 더 노출되어보는 것은 어떨까.

  

DVD 급의 영상을 madVR를 통해 후처리를 한다고 해서 블루레이 급의 영상보다 좋을 수가 없으므로, 처음부터 품질이 좋은 영상을 보는
것이 madVR를 사용하는 것보다 훨씬 화질이 좋다. SD를 개선한 것이 HD이므로 이는 당연한 이야기다. 그런데 '처음부터 품질이 좋은
영상'에 또 madVR을 쓰면 어떨까? madVR은 SD 뿐만 아니라 HD 영상에서도 좋은 영향을 끼친다. 더 좋았으면 좋았지 나쁠게 없다.
<del>즉 **자신의 오래된 영상을 많이 가지고 있고, 자신 PC 사양이 주체할 수 없을 만큼 좋아서 오래된 영상을 조금이라도 개선된
화질로 보고 싶으면 사용하는 것이 바로 madVR 렌더러이다**. 이는 음악 플레이어의 디코더가 상향평준화되어서 실제로 어떤 음악 플레이어를
고르더라도 똑같은 음원이면 똑같은 소리가 나오는 것 같은 것과 비슷한 현상이다.</del> 디코더는 상향평준화의 개념이라기 보다는 인코딩된
것을 '제대로' 디코딩하는 디코더를 사용한다면 결과물은 같다. 오래된 디코더들의 성능이 제각각인 것은 그 디코더들이 제대로 만들어지지 않았기
때문이다. 그리고 madVR은 렌더러이지 디코더가 아니다.<del>아 WASAPI나 [ASIO](ASIO.md)라고 해야 되는
거였는데: WASAPI ASIO는 입출력 매커니즘일 뿐, '디코딩' 또는 '렌더링'과 직접적인 관련은 없다</del> 또한 madVR이 높은
PC성능을 요구하는 것은 맞지만 어느 정도의 수준이지 극단적인 성능을 요구하는 것은 아니며, 오래된 SD 이하의 영상 뿐만 아니라 1080p
수준의 영상에도 효과가 있다. 또한 madVR은 타협적인 기능도 있어서, 사양이 좋지 못할 경우 화질을 조금 포기하고 속도를 가져갈 수도
있다. 그리고 '움직임'에 관한 떨림 제거 기능을 빠트리고 이야기하는 것은 madVR 기능의 절반만 이야기하는 셈이 된다.
<del>다만,[애니메이션](%EC%95%A0%EB%8B%88%EB%A9%94%EC%9D%B4%EC%85%98.md)에서 8bit와
10bit는 모니터가 10bit를 지원한다면 체감이 가능한 수준이기에, 오덕들은 써봐도 나쁘지 않을 듯 하다.</del> madVR은
최종적으로 8bit로 출력하므로 10bit 애니메이션에 대한 풍문은 madVR을 제대로 이해하지 못한 환상에 가까운 이야기이다. 제대로
10bit를 처리하려면 그래픽카드부터 10bit를 지원해야 한다. 8bit로 출력하는 렌더러 madVR을 쓰면서 10bit 애니메이션에서
화질 개선이 눈에 띈다는 것은 그만큼 madVR이 제대로 만들어졌고 그 렌더링 성능이 뛰어나다는 뜻이다.

  

주된 기능으로는, 동영상의 압축된 색상 정보를 업스케일링하고, 동영상의 화면 크기를 확대/축소할 때 고품질의 알고리즘을 적용하고, 모니터의
초당 주사율(보통 60Hz)과 동영상의 초당 프레임(보통 24fps)의 차이 때문에 생기는 화면 떨림 현상(Motion judder)을
줄이고, 모니터의 캘리브레이션 정보를 활용하고, 그라데이션으로 표현된 화면의 계단현상을 줄이고(deband), 고품질의 YUV -> RGB
변환을 수행하며, 최종 출력 시의 디더링 알고리즘을 선택할 수 있는 등, 화질을 위한 여러 가지 고품질의 기능을 제공한다.

  

madVR은 [그래픽 카드](%EA%B7%B8%EB%9E%98%ED%94%BD%20%EC%B9%B4%EB%93%9C.md)의 물리적인
성능을 (3D 연산 기능까지) 최대한 활용하는 것이 개발 목적이자 방향이기 때문에, 그래픽 카드의 사양을 꽤 많이 타는 편이다. GPU
성능은 물론이고 그래픽 카드에 장착된 RAM의 용량과 속도에도 영향을 받는다. CPU는 GPU보다는 덜 사용하는 편이며, 시스템의
RAM보다는 그래픽 카드의 RAM이 좀 더 중요하다. madVR의 설정 옵션은 선택지가 넓은 편이기 때문에 [그래픽카드](%EA%B7%B8%EB%9E%98%ED%94%BD%20%EC%B9%B4%EB%93%9C.md)가 별로 좋지 않다면 경우에 따라서
옵션을 타협하는 것도 가능하다. 다만, 옵션을 타협한 만큼 madVR의 효과는 줄어들기 때문에 테스트를 통한 적절한 선택이 필요하다.

  

주로 [팟플레이어](%ED%8C%9F%ED%94%8C%EB%A0%88%EC%9D%B4%EC%96%B4.md)와 [MPC-HC](Media%20Player%20Classic.md)를 동영상 플레이어로 많이 사용하며, 디코더로
[LAVFilters](LAVFilters.md)를 같이 넣어서 사용하는 경우가 많다. (제작자 포럼을 살펴보면 madVR 제작자와
LAVFilters 제작자가 서로 교류하는 모습도 볼 수 있다.) 자막의 경우 플레이어 자체의 자막 기능을 사용해도 무방한데, 일부
플레이어에서는 화면 캡쳐 시에 자막이 캡쳐되지 않는 현상이 있다. 이럴 경우, 플레이어 자체 자막 기능은 끄고, 자막 필터로 [xy-
VSFilter](http://forum.doom9.org/showthread.php?t=168282)를 사용하면 해결된다. xy-
VSFilter는 madVR과 협력하여 개발되는 자막 필터인데, madVR 사용시에 궁극적으로 권장되는 자막 필터이다.외산인 만큼
smi문제에 시달릴 것이라고 생각할 수 있으나,smi 역시 정상 출력된다.

  

madVR의 각 옵션의 구체적인 설명과 설정법은 [여기](http://varins.com/394)를 참고하면 되는데, madVR은 사양을
많이 타므로 자신의 시스템에 맞게 적절하게 설정하는 것이 필수적이다.

