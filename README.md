# MLLearn

本项目用于记录机器学习与深度学习的学习过程，包括经典机器学习算法实例、《机器学习》（西瓜书）代码实践，以及 Datawhale PyTorch 教程练习。项目以 Jupyter Notebook 为主，适合按目录逐项阅读和运行。

## 项目结构

```text
MLLearn/
├── machinelearning/       # 经典机器学习算法与数据集实例
├── code_WatermelonBook/   # 《机器学习》（西瓜书）章节代码实践
└── pytorch_Datawhale/     # Datawhale《深入浅出 PyTorch》学习笔记
```

## 经典机器学习案例

`machinelearning` 目录包含以下五个完整案例：

| 目录 | 算法与任务 | 主要文件 |
|---|---|---|
| `01LinearRegress_Bostonhouse` | 线性回归：波士顿房价预测 | `train_boston.ipynb`、`course-5-boston.csv` |
| `02LogisticandPerceptron_diabetes` | 逻辑回归与感知机：糖尿病分类 | `train_diabetes.ipynb`、`diabetes.csv` |
| `03KNN_syringa` | K 近邻：鸢尾花分类 | `train_syringa.ipynb`、`syringa.csv` |
| `04NaiveBayes_spamemails` | 朴素贝叶斯：垃圾邮件分类 | `train_spam.ipynb`、`trec06c/`、`stopwords.txt` |
| `05SVM_faces` | 支持向量机：人脸识别 | `train_face.ipynb` |

垃圾邮件案例已包含 `trec06c/` 数据目录，因此首次克隆可能需要较长时间。人脸识别案例使用的 LFW 数据由 scikit-learn 在首次运行时下载到本地 `lfw_home/`；该缓存目录通过自身的 `.gitignore` 排除，不上传到仓库。

## 西瓜书代码实践

`code_WatermelonBook` 保存《机器学习》（西瓜书）相关章节的 Notebook，包括第 2～11 章的部分算法实现与实验。建议结合对应章节阅读，并在独立 Conda 环境中运行。

## Datawhale PyTorch 学习

`pytorch_Datawhale` 包含以下内容：

1. PyTorch 模型构建；
2. 模型训练与测试；
3. 基础实践；
4. Fashion-MNIST 实例；
5. 自定义模型；
6. 训练技巧；
7. PyTorch 可视化。

## 运行方式

推荐使用 Conda 创建独立环境：

```bash
conda create -n mllearn python=3.10 -y
conda activate mllearn
conda install -c conda-forge jupyterlab numpy pandas scipy matplotlib seaborn scikit-learn -y
```

运行 PyTorch 相关 Notebook 时，还需根据本机 CPU、CUDA 和驱动版本安装匹配的 PyTorch。其他 Notebook 可能使用 `Pillow`、`imbalanced-learn`、`gensim`、`jieba`、`tqdm`、`torchvision` 等扩展包，可根据 Notebook 的导入提示安装。

在项目根目录启动 Jupyter：

```bash
jupyter lab
```

然后进入对应目录打开 `.ipynb` 文件。建议从项目根目录启动，避免 Notebook 中的相对数据路径失效。

## 使用说明

- Notebook 主要用于学习和实验，运行结果可能因依赖版本、随机种子或硬件环境不同而略有差异。
- 数据文件仅用于课程学习和算法验证；如需再分发或用于其他用途，请确认原始数据集的许可条款。
- 运行训练任务前，请检查数据路径以及 Notebook 中的 CPU/GPU 设置。

## 学习资料

- Datawhale：《深入浅出 PyTorch》
- 周志华：《机器学习》
- scikit-learn 官方文档
- PyTorch 官方文档
