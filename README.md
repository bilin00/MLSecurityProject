# MLSecurityProject
# I. Files
```
├── data
    ├── Multi-trigger Multi-target
        └── eyebrows_poisoned_data.h5
        └── lipstick_poisoned_data.h5
        └── sunglasses_poisoned_data.h5
    └── anonymous_1_poisoned_data.h5
    └── clean_test_data.h5
    └── clean_validation_data.h5
    └── sunglasses_poisoned_data.h5
├── models
    └── sunglasses_bd_net.h5
    └── sunglasses_new_model.h5
    └── multi_trigger_multi_target_bd_net.h5
    └── multi_trigger_multi_target_new_model.h5
    └── anonymous_1_bd_net.h5
    └── anonymous_1_new_model.h5
    └── anonymous_2_bd_net.h5
    └── anonymous_2_new_model.h5
├── Fine-pruning and Evaluation
    └── sunglasses_bd_net.ipynb
    └── multi_trigger_multi_target_bd_net.ipynb
    └── anonymous_1_bd_net.ipynb
    └── anonymous_2_bd_net.ipynb
└── evaluation script
    └── eval.py
    └── eval_anonymous_1.py
    └── eval_anonymous_2.py
    └── eval_multi_trigger_multi_target.py
    └── eval_sunglasses.py
```
# II. Dependencies
# III. Validation Data
1. Download the validation and test datasets from here and store them under data/ directory.
2. The dataset contains images from YouTube Aligned Face Dataset. We retrieve 1283 individuals each containing 9 images in the validation dataset.
3. sunglasses_poisoned_data.h5 contains test images with sunglasses trigger that activates the backdoor for sunglasses_bd_net.h5. Similarly, there are other .h5 files with poisoned data that correspond to different BadNets under models directory.
# IV. Evaluating Operation
1. To evaluate the fine-purning model with giving data, execute eval.py by running: python3 eval.py . E.g., python3 eval.py data/testing_data.h5 models/sunglasses_new_model.h5 models/sunglasses_bd_net.h5
2. To evaluate the repaired network with given input of YouTube Face image by running the corresponding .py by running: E.g., python3 eval_anonymous_2.py data/test_image.jpg
