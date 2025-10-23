<br/>

# GPU 사용률 확인 
<br/>

GPU를 사용하는 노드의 GPU 사용률을 확인하기 위해 <br/>
아래 명령으로 해당 노드의 디버그 파드를 생성한다. <br/>
<br/>

~~~
% kubectl debug node/<노드이름> -n <네임스페이스> -it --image=nvidia/cuda:13.0.1-base-ubuntu24.04 -- bash
~~~
<br/>

> * 디버그 파드를 생성하기 위한 이미지 버전은 아래 도커허브에서 참조.
>    - https://hub.docker.com/r/nvidia/cuda

<br/><br/>
디버그 파드가 생성 되면서 해당 파드에 바로 접속하게 된다. <br/>
디버그 파드 접속 후 아래 명령으로 GPU 사용률을 확인할 수 있다.
<br/><br/>

~~~
% nvidia-smi
~~~
~~~
% nvidia-smi -l 1
~~~

<br/><br/><br/>

