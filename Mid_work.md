# 中期作业实验报告
### （数据说明：数据为地图上的经度和纬度）
## 一、数据处理  
### 1、在地图上画出定位点   
  ```{r}
data_model<-read.csv("df3.csv",header = T)
data_model_5 <- data_model[,5:6]
plot(data_model_5,main="sample number",xlab="",ylab="")

```     
### 二、聚类

#### 1、使用K-means算法对坐标起点聚类
####  起点数据的原始样本点
  ```{r}
data_model<-read.csv("df3.csv",header = T)
data_model_5 <- data_model[,5:6]
plot(data_model_5,main="sample number",xlab="",ylab="")

```   

#### k=2时，起始点的聚类效果图
  ```{r}
KMClu1<-kmeans(data_model_5,centers=2)
plot(data_model_5,col=(KMClu1$cluster+1),main="K-Means聚类K=2",xlab="",ylab="",pch=20,cex=1.5)
``` 

####  k=3时，起始点的聚类效果图
  ```{r}
KMClu1<-kmeans(data_model_5,centers=3)
plot(data_model_5,col=(KMClu1$cluster+1),main="K-Means聚类K=3",xlab="",ylab="",pch=20,cex=1.5)
```

####  k=4时，起始点的聚类效果图
  ```{r}
KMClu1<-kmeans(data_model_5,centers=4)
plot(data_model_5,col=(KMClu1$cluster+1),main="K-Means聚类K=4",xlab="",ylab="",pch=20,cex=1.5)
```

####  结论
##### 通过以上去不同的K值可以发现，K=3时聚类效果是比较好的。

#### 2、使用K-means算法对坐标终点聚类

####终点数据的原始样本点
  ```{r}
data_model<-read.csv("df3.csv",header = T)
data_model_5 <- data_model[,7:8]
plot(data_model_5,main="sample number",xlab="",ylab="")

```   

#### k=2时，终点的聚类效果图
  ```{r}
KMClu1<-kmeans(data_model_5,centers=2)
plot(data_model_5,col=(KMClu1$cluster+1),main="K-Means聚类K=2",xlab="",ylab="",pch=20,cex=1.5)
``` 

####  k=3时，终点的聚类效果图
  ```{r}
KMClu1<-kmeans(data_model_5,centers=3)
plot(data_model_5,col=(KMClu1$cluster+1),main="K-Means聚类K=3",xlab="",ylab="",pch=20,cex=1.5)
```

####  k=4时，终点的聚类效果图
  ```{r}
KMClu1<-kmeans(data_model_5,centers=4)
plot(data_model_5,col=(KMClu1$cluster+1),main="K-Means聚类K=4",xlab="",ylab="",pch=20,cex=1.5)
```

####  结论
##### 通过以上去不同的K值可以发现，K=2和K=4时聚类效果是比较好的。

#### 3、使用K-means算法对坐标OD聚类
####  OD数据的原始样本点
  ```{r}

```    

### 链接   
<http://rpubs.com/loness/167347>   
[点击查看](http://rpubs.com/loness/167347)   


### 其他
1. 注意新行是在每行的末尾加两个以上的空格
2. 可以在markdown中插入HTML，但不是R代码中。例如:<a  href="http://rpubs.com/loness/167347">点击进入</a>
