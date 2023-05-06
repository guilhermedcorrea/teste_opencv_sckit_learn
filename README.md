##Execução do projeto
<br>criar venv: py -3 -m venv venv<br/>
<br>ativar: venv\Scripts\activate<br/>
<br>instalar dependencias: pip freeze > requirements.txt<br/>



#exemplo parametro

```python
image_names = []
x_image = []
y_label = []

labels = os.listdir(data_path)
cont = len(labels)
i = 0
while i < cont:
    try:
        if '.jpg' in labels[i]:
            if labels[i] != None:
                image_names.append(labels[i])
                image = cv2.imread(os.path.join(data_path,labels[i]))
                image = cv2.resize(image, (300,300))
                x_image.append(image.flatten())
                y_label.append(labels[i])
                print(image)
    except:
        pass   
    i +=1
```

<br>Intera na pasta com as imagens e faz a leitura dos arquivos<br/>