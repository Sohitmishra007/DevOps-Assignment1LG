# DevOps Assignment 🚀

This project demonstrates end-to-end DevOps using a 2-tier application deployed on AWS using Terraform, Docker, CI/CD pipelines, CloudWatch, IAM, and ALB for load balancing.

---

## 📁 Project Structure

- `backend/` - Python FastAPI app with /health and /api/message
- `frontend/` - Next.js app calling backend APIs
- `terraform/` - Infrastructure-as-code for AWS (ECS, ALB, VPC, IAM)
- `.github/workflows/` - CI/CD with GitHub Actions
- `docker-compose.yml` - For local dev and testing

---

## ✅ Features Implemented

- [x] Git-based workflow with `main`, `develop`, and `feature/*`
- [x] Backend & Frontend containerized using Docker (multi-stage builds)
- [x] CI/CD pipeline with GitHub Actions
- [x] Terraform to provision ECS, ALB, ECR, Secrets Manager, IAM
- [x] Monitoring via CloudWatch Dashboards & Alarms
- [x] Load balancing with ECS Fargate + ALB

---

## 🚀 Deployment URLs

- **Frontend:** http://app-load-balancer-783029873.us-east-1.elb.amazonaws.com
- **Backend:** http://app-load-balancer-783029873.us-east-1.elb.amazonaws.com/api/message

---

---

## 🧪 CI/CD Logs

CI builds, tests, and deploys on push to `develop` and merge to `main`.

- ✅ Unit tests via `pytest`
- ✅ Frontend tests using build validation
- ✅ Docker images tagged with commit SHA and pushed to ECR

---

## 🔒 Security & IAM

- Fine-grained IAM roles for tasks
- Secrets stored and accessed securely from AWS Secrets Manager

---

## 📊 Monitoring

- CloudWatch Dashboards for:
  - CPUUtilization
  - MemoryUtilization
  - RequestCount
- Alarm for CPU > 70% for 5 minutes

---

## 📦 How to Run Locally

```bash
# Backend
cd backend && uvicorn main:app --reload

# Frontend
cd frontend && npm install && npm run dev
