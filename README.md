# 🧠 Générateur Automatique de Légendes d’Images

Projet de génération de descriptions automatiques d'images à l’aide d’un modèle de Deep Learning combinant **ResNet-50** pour l’extraction des caractéristiques et **LSTM** pour la génération de texte, entraîné sur le dataset **COCO 2017**.  
L’application finale est déployée avec **Streamlit** pour permettre à l’utilisateur de charger une image et recevoir une légende générée automatiquement.

---

## 🎓 Informations Académiques

- **Encadrant :** Pr.MAHMOUDI Abdelhak
- **Réalisé par :** EL MOUTAOUAKIL Khalid & HAMOUDAN Badreddine

- **Filière :** Master Informatique et Télécommunications  
- **Établissement :** Faculté des Sciences – Université Mohammed V – Rabat  
- **Année universitaire :** 2024 – 2025

---

## 🚀 Lien vers la Démo

🔗 [Tester l'application en ligne sur Streamlit](https://captionify.streamlit.app/)

---

## 🖼 Exemple de Résultat

| Image Uploadée | Légende Générée |
|----------------|------------------|
| ![exemple](exemples/chat.jpg) | "Un chat est allongé sur un coussin gris." |

---

## 🛠 Fonctionnalités

- Upload d’image via :
  - Fichier local
  - Caméra
  - Lien URL
- Génération de légendes automatiques
- Interface intuitive via Streamlit
- Support du modèle pré-entraîné (ResNet-50 + LSTM)

---

## 📦 Installation locale

### 1. Cloner le dépôt

```bash
git clone https://github.com/khalid18031987/image-captioning.git
cd image-captioning

### 2. Créer et activer un environnement virtuel

```bash
python -m venv monenv
# Windows :
monenv\Scripts\activate
# Linux/macOS :
source monenv/bin/activate
```

### 3. Installer les dépendances

```bash
pip install -r requirements.txt
```

---

## 📁 Préparation du dataset COCO 2017

Téléchargez les fichiers suivants depuis [cocodataset.org](https://cocodataset.org/#download) :

- train2017.zip
- val2017.zip
- test2017.zip
- annotations_trainval2017.zip
- image_info_test2017.zip

Décompressez-les dans un dossier nommé `coco_dataset/` à la racine du projet.

---

## 🧠 Entraînement du modèle

1. Lancer le notebook d’entraînement :
```bash
jupyter notebook training.ipynb
```

2. Une fois l’entraînement terminé, renommer les fichiers du dossier `models/` :
```bash
encoder-final.pkl → encoder.pkl
decoder-final.pkl → decoder.pkl
```

---

## 🖥️ Lancer l’application

```bash
streamlit run app.py
```

Ouvrez ensuite l’interface dans votre navigateur (généralement [http://localhost:8501](http://localhost:8501)).

---

## 🗂 Structure du projet

```
image-captioning/
│
├── app.py
├── training.ipynb
├── requirements.txt
├── vocab.json
│
├── models/
│   ├── encoder.pkl
│   └── decoder.pkl
│
├── coco_dataset/
│   ├── train2017/
│   ├── val2017/
│   ├── test2017/
│   └── annotations/
│
├── imgcaptioning/
│   ├── coco_dataset.py
│   ├── model.py
│   ├── pipeline.py
│   ├── tokenizer.py
│   ├── utils.py
│   └── vocabulary.py
```

---

## 📹 Présentation Vidéo

🎥 Une vidéo explicative de **7 minutes** est disponible, intégrant :
- L’installation de l’environnement
- Les explications du code
- Une démonstration en temps réel

[🔗 Accéder à la vidéo sur Google Drive](https://drive.google.com/drive/folders/1nKXCG6i83RCjmf6pTOSpsY7va7zW68NI?usp=sharing)

---

## 📄 Rapport du Projet

📝 Le rapport complet du projet (10 pages max) est téléchargeable ici :

[📂 Rapport Word sur Google Drive](https://drive.google.com/drive/folders/1nKXCG6i83RCjmf6pTOSpsY7va7zW68NI?usp=sharing)

---

## 🙌 Remerciements

Ce projet a été réalisé avec le soutien du **Laboratoire d’Informatique** de la FS Rabat et l’encadrement pédagogique du **Pr.MAHMOUDI Abdelhak**.
