## RADAR: Defending RAG Dynamically against Retrieval Corruption

### Structure

```
├── README.md
|
├── requirements.txt
|
├── Static   	# Static RAG Defense via Single-Step Min-Cut
|   ├── src
|		├── data
|   ├── main.py
└── Dynamic   # Dynamic RAG Defense with Memory Node
    ├── src
    └──main.py
```

### Dependencies

```
pip install -r requirements.txt
```

### Usage

#### Static

```
python static/main.py \
  --model_name deepseek-chat \
  --dataset_name realtimeqa \
  --top_k 10 \
  --defense_method mincut \
  --attack_method PIA \
  --attackpos 0
```

#### Dynamic

```
python dynamic/main.py \
  --model_name deepseek-chat \
  --defense_method mincut \
  --attack_method PIA \
  --attackpos 0 \
  --top_k 50 \
  --save_response \
  --attack_each_step
```

