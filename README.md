# Custom VLM Design for Industrial Quality Inspection

## Overview
This assignment focuses on designing a custom Vision-Language Model (VLM) for PCB quality inspection.  
The system is required to work offline, answer natural language questions about PCB defects, and provide defect locations with confidence scores.

---

## Problem Statement
A semiconductor manufacturer needs an AI-based inspection system for PCBs.  
The system should detect defects, answer inspector queries, avoid hallucinations, and respond within 2 seconds using only available PCB images and bounding box annotations.

---

## Model Selection
A BLIP-2 based custom VLM architecture is selected for this task.  
It provides better control over vision and language components, supports fast inference, and reduces hallucination compared to generic VLMs.

---

## Design Strategy
The system uses a vision encoder trained on PCB defect images and a lightweight language decoder.  
A defect detection head ensures that all answers are grounded in detected visual evidence.

---

## Optimization
To meet offline and speed requirements, techniques like quantization, pruning, knowledge distillation, and LoRA are used.  
These methods reduce model size while maintaining accuracy and fast inference.

---

## Hallucination Control
The model is trained to answer only when a defect is detected.  
Structured outputs and confidence thresholds prevent the model from guessing or providing false information.

---

## Training Approach
Training is done in multiple stages, starting with defect detection.  
Question–answer pairs are automatically generated from defect labels, and data augmentation improves robustness.

---

## Validation
Model performance is validated using localization accuracy (IoU), defect counting accuracy, hallucination rate, and inference time.  
This ensures the system is reliable for industrial use.

---

## Conclusion
This assignment presents a simple and practical design for a custom VLM tailored to PCB inspection.  
The approach is suitable for a fresher-level project and meets industrial constraints effectively.
