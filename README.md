# Comp_neuro_final

```
Comp_neuro_final/
├── README.md               # 프로젝트 개요·설치·실행 방법 
│
├── envs/                   # 커스텀 환경 모듈  
│   └── custom_maze_env.py  # 환경 정의
│   └── get_retina_image.py # 시각 이미지 랜더링
│
├── src/                    # 핵심 모델 코드  
│   ├── memory/             
│   │   ├── slots.py        # Slot 클래스 정의 (obs, Δt, h)  
│   │   ├── bank.py         # MemoryBank 인터페이스  
│   │   └── forget.py       # 망각곡선·noise 로직  
│   │
│   ├── retrieval/          
│   │   ├── attention.py    # attention 유사도 함수·key/value  
│   │   └── gate.py         # Retrieval Gate 모듈  
│   │
│   ├── model/              
│   │   └── rnn_agent.py    # RNN+retrieval 통합 모델  
│   │
│   └── utils/              
│       ├── logger.py       # 로그·tensorboard 유틸  
│       └── metrics.py      # 평가 지표 함수  
│
├── experiments/            # 실험 스크립트 & 설정  
│   ├── configs/            
│   │   ├── default.yaml    # 기본 하이퍼파라미터    
│   │
│   ├── train.py            # 학습 실행 엔트리포인트  
│   ├── test.py             # 테스트/평가 스크립트  
│   └── analyze.py          # 결과 수집·시각화 자동화    
│
├── notebooks/              # 탐색·분석용 Jupyter 노트북  
│   ├── visualize_map.ipynb  
│   ├── env_test.ipynb  
│   └── performance_comparison.ipynb  
│
├── results/                # 실험 결과 산출물  
│   ├── logs/               # TensorBoard 로그 등    
│   ├── checkpoints/        # 모델 체크포인트    
│   └── figures/            # 학습곡선·히스토그램·Heatmap    
│
└── scripts/                # 편의용 실행 스크립트  
    ├── run_all.sh          # 일괄 학습/테스트    
    └── env_setup.sh        # 가상환경·데이터 다운로드  
```
