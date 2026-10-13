---
title: '[DS] 5. Unsupervised Learning'
categories:
- Study
- 24-2
- DataScience
tags:
- Data Science
date: 2024-10-08 00:00:00 +0900
permalink: /study/2024-2/data-science/5/
math: true
archive_source: Yuris99/past-blog
archive_source_path: _posts/Study/24-2/DataScience/2024-10-08-5.md
archive_source_commit: e65436978e96e9427b0c30bc6b8b754ccd8c6eb7
---

[> Go to Data Science Contents]({{ '/study/2024-2/data-science/' | relative_url }})

# Clustering
## Unsupervised Learning
Label이 없음, Input data만 있다.
Data로 특정 패턴 structrue를 뽑을 때 사용한다.

## K-Means clustering
![5 kmeans]({{ '/assets/archive/past-blog/DS/5_kmeans.png' | absolute_url }})     

어떤 Input을 찍고, 각각의 데이터가 어떤 점과 가까이 있는지 비교해가면서 학습하는 과정.      

1. Compute cluster assignment(가장 가까운 평균 점, latent variable 구하기), Expectation:
$z^{(i)} = \underset{j}{\text{argmin}} \|\|\mu^{(j)}-x{(i)}\|\|^2_2, i=1, ..., m$   
2. Re-compute means:
$\mu^{(j)} \leftarrow \text{Mean}(\{ x^{(i)}\|z^{(i)}=j \}  ) j=1, ..., k$      
반복하기!       

Starting point가 매우 중요하다!       
몇개를 해야하는지는 해봐야 안다...(목적에 따라 정하기)      

## ㄷExpectation Maximization (EM)
- E-step: Estimate the missing latent variable
  - missing된 Latent variable 찾기
- M-step: Maximize the parameters in the presence of the data and latent variable
  - parameter 최대화
반복!


# Gaussian Mixture Model (GMM)
## Probability Density Function
- Parametric density estimation
  - Parameter를 가지고 있는 모델을 가지고 예측
- Non-parametric density estimation

## EM for GMM
- Gaussian의 개수 K
- k번째 Gaussian의 매개변수 $(\mu_k, \sum_k), k = 1, ..., K$
- k번째 Gaussian의 가중치 $\pi_k, k = 1, ..., K$

---

원문: [Yuris99/past-blog](https://github.com/Yuris99/past-blog/blob/e65436978e96e9427b0c30bc6b8b754ccd8c6eb7/_posts/Study/24-2/DataScience/2024-10-08-5.md) · [전체 학습 기록]({{ '/study/' | relative_url }})
