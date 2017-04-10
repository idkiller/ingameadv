# In Game 광고 인벤토리 개발의 문제

## 광고 Inventory를 표현하는 부분을 Component로 만들어 모듈화 해서 재사용 하기 힘들다.  

 1. 게임 엔진의 수가 매우 많다.
   - Source Engine, Unreal Engine, Unity, Amazon Lumberyard, CRY5, Cocos2D-X, Crocs, Fusion...
 2. 만드는 언어가 너무 다양하다.
   - C, C++, Javascript/Html, Java, Obj-C, C#, Lua...
 3. 플랫폼이 너무 다양하다.
   - Windows, Android, iOS, Web...

## 외부 광고와 다르게 In Game 광고는 게임의 스타일과 잘 어울려야 한다.

 1. 게임에서 원하는 리소스의 종류, 크기, 분위기 등이 모두 다르다. 리소스는 모두 돈이다.  
	 ![in game adv 1](https://github.com/idkiller/ingameadv/blob/master/ingame.jpg?raw=true)  
	 ![in game adv 2](https://github.com/idkiller/ingameadv/blob/master/ingame2.jpg?raw=true)  
	 ![in game adv 3](https://github.com/idkiller/ingameadv/blob/master/ingame3.jpg?raw=true)  
	 ![in game adv 4](https://github.com/idkiller/ingameadv/blob/master/ingame4.gif?raw=true)  
	 ![in game adv 5](https://github.com/idkiller/ingameadv/blob/master/ingame5.jpg?raw=true)  
	 ![in game adv 6](https://github.com/idkiller/ingameadv/blob/master/ingame6.jpg?raw=true)  
	 ![in game adv 7](https://github.com/idkiller/ingameadv/blob/master/ingame7.jpg?raw=true)  

 2. 게임 리소스는 보통 아껴쓰게 되지만, 동영상 광고등은 추가적인 컴퓨팅 파워를 차지할 수 있다.


## 측정이 힘들다.

 1. 모듈에서 게임과는 별개로 네트웍 리소스에 접근 해야 한다.  
 2. 외부 광고와 다르게 같은 Process에서 네트웍 접근을 할 가능성이 크다.  
 3. 빠르게 움직이는 게임의 경우 (FPS등) 어떻게 노출 빈도를 카운팅 할 것인가?

## Cheating을 막을 수 있는가?

 게임 개발자가 광고 노출 결과에 비해 많은 카운팅을 하는 것을 막을 수 있는가?
 
## 예상 해결 방법
 1. 대중적인 몇가지 엔진용 컴포넌트만을 만든다. Unreal Engine, Unity, Cocos2D-X, CRY5
 2. 한정적인 언어만 지원한다. C/C++/Javascript
 3. 한정적인 플랫폼만 지원한다. Windows, Android, iOS
 4. 쉬운 리소스 편집 툴을 제공한다.
 5. 다양한 사이즈의 동영상, 이미지를 제공한다.
 6. ML로 이미지 리소스를 자동으로 게임에 맞게 바꾼다?
 7. Module을 최대한 가볍고 잘 만든다.
