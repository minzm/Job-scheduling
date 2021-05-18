# Job-scheduling

1. Job Scheduling 문제

  Job Scheduling 문제는 n개의 작업, 각 작업의 수행 시간 ti, i = 1,2,3,…,n, 그리고 m개의 동일한 기계가 주어질 때, 모든 작업이 가장 빨리 종료되도    록 작업을 기계에 배정하는 문제이다. 단, 한 작업은 배정된 기계에서 연속적으로 수행, 기계는 1번에 하나의 작업만을 수행한다. 작업 스케줄링 문제를 해 결하기 위한 가장 간단한 방법은 그리디 알고리즘을 이용하는 것이다. 즉, 배정된 작업이 가장 빨리 끝나는 기계에 새 작업을 배정하는 것이다.
  
2. Algorithm

  입력: n개의 작업, 각 작업 수행 시간 ti, i= 1,2,…,n, 기계 Mj, j = 1,2,…,m
  
  출력: 모든 작업이 종료된 시간
 
 
 3. 시간 복잡도
 
   작업 스케줄링 알고리즘의 시간 복잡도는 작업들을 정렬하는데 O(nlogn)걸리고, while 루프에서는 직업을 jobs에서 가져가다 수행 가능한 기계를 찾아서 배정하므로 O(m)시간이 걸린다. 단, m은 사용된 기계의 수, while루프가 수행된 총 횟수는 n번이므로, n×O(m) = O(mn)시간이 걸린다. 따라서 작업 스케줄링 알고리즘의 시간 복잡도는 O(nlogn) + O(mn)이다.  
    
 4. 근사 비율
 
     근사해를 OPT’, 최적해를 OPT이라고 한다면 OPT’ <= 2*OPT이다.
 
 5. code
 
 ```java
 package jobschedule;

import java.io.BufferedReader;

public class JobSchedule{
    private ArrayList<Machine> ms;            // 기계 리스트

 public void schedule(){
    ArrayList<Job> jobs = getJobs();          // 작업 스케줄 리스트 
    arraysort(jobs);                          // 시작 시간이 가장 빠른것부터 sorting하기
    ms = new ArrayList<Machine>();
    int index = 0; 
    Job job;  
    
    while(index < jobs.size()) {              // 리스트 마지막까지 
      job = jobs.get(index);                  // 시작시간이 가장 이른 작업 job을 가져옴
      if () {}
    }
          .
          .
          .
   
```

