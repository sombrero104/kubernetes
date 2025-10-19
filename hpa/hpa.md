<br/>

# HPA 오토스케일러 테스트
<br/>

## HPA (HorizontalPodAutoscaler)
워크로드의 크기를 수요에 맞게 자동으로 스케일링한다. <br/>
수평 스케일링(HPA, HorizontalPodAutoscaler)은 부하 증가에 대해 파드를 더 배치하는 것을 뜻한다. <br/>
이는 수직 스케일링(VPA, VerticalPodAutoscaler) 과는 다른데, <br/>
쿠버네티스에서 수직 스케일링은 이미 실행 중인 파드에 더 많은 리소스(메모리/CPU)를 할당하는 것을 뜻한다. <br/>
<br/><br/>

### 샘플 애플리케이션 서비스 생성 
~~~
kubectl apply -f https://k8s.io/examples/application/php-apache.yaml
~~~

### HPA 오토스케일러 생성 
~~~
kubectl autoscale deployment php-apache --cpu-percent=50 --min=1 --max=10
~~~

<img src="./images/hpa-test-01.png" width="80%" /><br/>
<br/><br/>

#### * 참조
https://kubernetes.io/ko/docs/tasks/run-application/horizontal-pod-autoscale/ <br/><br/>
https://kubernetes.io/ko/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/ <br/>

<br/><br/><br/><br/>

