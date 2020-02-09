## replicaSet LifeCycle
Pod 개수만 수정해서는 replicaSet 가 새로 생성되지 않는다. (=revision 이 변경되지 않는다.)
컨테이너의 이미가 수정된다면, 기존의 Pod 는 단계적으로 정지되고 새로운 Pod 가 생성된다.


``` bash 
# 직전 버전으로 롤백하기
$ kubectl rollout undo deployment echo
deployment.extensions/echo rolled back
```

