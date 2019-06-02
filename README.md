# OpenCVnAndroidPart1

Android에서 OpenCV를 간단히 사용할 수 있도록 구성한 소스 입니다.



## 사용한 소스

OpenCV의 이미지를 블랙에 회색 선으로 외각을 표시하는 기능을 구현하였습니다.

```java
public void detectEdge(){
//OpenCV 에서 작업할 수 있도록 bitmap을 Mat으로 변경합니다.
Mat src = new Mat();
Utils.bitmapToMat(bitmap, src);

Mat edge = new Mat();
Imgproc.Canny(src, edge, 50, 150);

Utils.matToBitmap(edge, bitmap);

src.release();
edge.release();
}
```

