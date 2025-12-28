# MLOPS-End-to-End-Pipeline-and-DVC

    This Project will cover detailed understanding of end to end ML Pipeline and working around using DVC for experiment tracking and Data versioning(AWS S3).

    Stage 1: Building (MLOPS) Pipeline
            Data Preprocessing--> Feature Engineering -->Model Building --> Model Evaluation.
            (Added logs and exception handling as well..)

    Stage 2: From above stages you cannot just run each and ever module individually, so we can use dvc.yaml file to run these modules.
            dvc.yaml (dvc init-->dvc repro-->dvc dag) -->params.yaml

    Stage 3: Creating a params.yaml file for getting parameters from a specific file
            dvc.yaml--> configurations(data_ingestion:
                                            test_size: 0.25

                                            feature_engineering:
                                            max_features: 30

                                            model_building:
                                            n_estimators: 26
                                            random_state: 2)
                                            
    Stage 4: Expermients with DVC
            dvclive installed --> dvc exp run (to perform different experiment using multiple combination of parameters)
            ---> vs-code( installed dvc extension to observe different experiments)