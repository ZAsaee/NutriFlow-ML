# NutriFlow Project - AWS Permission Reference

This document outlines the IAM role and S3 access configuration used in the NutriFlow End-to-End pipeline.

---

## SageMaker Execution Role

**Role Name:**
'AmazonSageMaker-ExecutionPolicy-20250601T163722'

**Used for:**
- SageMaker Studio Notebook
- Training Jobs
- Pipelines
- S3 access

---

## S3 Bucket Configuration

**Bucket Name:**  
`nutriflow-pipeline`

**Purpose:**  
Stores raw and processed data, model artifacts, and pipeline outputs.


---

## ✅ Custom Inline Policy for Role

Attached to `AmazonSageMaker-ExecutionRole-...`:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:PutObject",
        "s3:GetObject",
        "s3:ListBucket"
      ],
      "Resource": [
        "arn:aws:s3:::nutriflow-pipeline",
        "arn:aws:s3:::nutriflow-pipeline/*"
      ]
    }
  ]
}
