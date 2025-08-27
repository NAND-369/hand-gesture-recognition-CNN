# Hand Gesture Recognition using CNN  

This project implements a **Convolutional Neural Network (CNN)** for recognizing **American Sign Language (ASL)** hand gestures. The system classifies grayscale images of hand signs (A–Z, excluding J and Z due to motion) into their respective letters, aiming to support communication accessibility for the hearing-impaired.  

---

##  Dataset  
- **Images:** 28×28 grayscale hand gesture images.  
- **Classes:** 26 letters (A–Z except J and Z).  
- **Format:** Similar to MNIST, with labeled training and testing sets.  

---

## Model Architecture  
The CNN consists of:  
1. **Conv Layer 1 & 2** – Extracts low- and high-level image features.  
2. **ReLU Activation** – Introduces non-linearity.  
3. **MaxPooling (2×2)** – Reduces spatial dimensions.  
4. **Fully Connected Layer** – Learns feature combinations.  
5. **Dropout (0.28)** – Reduces overfitting.  
6. **Output Layer (26 nodes, Softmax)** – Classifies into letters.  

- **Optimizer:** Adam  
- **Training:** 20 epochs  

---

##  Results  
- **Training Accuracy:** ~98%  
- **Testing Accuracy:** ~96%  
- **Loss & Accuracy Curves:** Show steady convergence.  
- **Overfitting Control:** Dropout improved generalization; additional dropout (0.4) further reduced variance.  

---

##  Observations  
- CNN captured hierarchical features effectively (from edges to complex patterns).  
- Pooling layers provided **translation invariance**, improving robustness.  
- Weight sharing reduced computational cost while maintaining accuracy.
- 
<img width="423" height="393" alt="download (1)" src="https://github.com/user-attachments/assets/eccd3109-7d8c-464b-b9ac-923623bce834" />

<img width="432" height="393" alt="download" src="https://github.com/user-attachments/assets/6ce1a2e4-e74e-45fb-8f02-77246c1b1dce" />


##  How to Run  
1. Clone repository:  
   ```bash
   git clone https://github.com/your-username/hand-gesture-recognition-cnn.git
   cd hand-gesture-recognition-cnn
