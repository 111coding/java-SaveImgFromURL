### 간편하게 이미지 URL 파일로 저장하기

- git주소 : <https://github.com/111coding/java-SaveImgFromURL>


### method 설명
- saveImg.saveImgFromUrl(imgUrl, path) : 이미지url과 저장경로로 저장(서버에 저장된 이미지파일이름으로 저장)
- saveImg.saveImgFromUrl(imgUrl, path, fileName) : 이미지url과 저장경로와 저장될이미지파일이름 지정
- getPath() : 저장된 경로 리턴
- getSavedFileName() : 저장된 파일이름 리턴



### 사용예제1(파일이름 지정X => 서버에 저장된 이름으로 저장)
```{.java}
package testArea;

import java.io.IOException;

import net.halowd.saveImg.SaveImg;

public class TestApp {
	public static void main(String[] args) {
		String imgUrl = "https://postfiles.pstatic.net/MjAxOTExMTZfMjQ2/MDAxNTczODQxNjg3NTYz.pXFjEQ3P8_uFgacA25iqWl0GnjCMQlpmbOvq4DS38AQg.6DIhw7fyF2fGYnWq-Qhx6qAqa98K4XWsAHsYg-9vrMIg.PNG.halowd/JSP.png?type=w966";
		String path = "C:/Users/LEE/Desktop/imgtest";

		SaveImg saveImg = new SaveImg();

		try {
			int result = saveImg.saveImgFromUrl(imgUrl, path); // 성공 시 1 리턴, 오류 시 -1 리턴
			if (result == 1) {
				System.out.println("저장된경로 : " + saveImg.getPath());
				System.out.println("저장된파일이름 : " + saveImg.getSavedFileName());
			}
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
	}
}

```
#### 3번 실행 시 콘솔 출력 내용
![saveImg]](https://postfiles.pstatic.net/MjAxOTExMThfMTU2/MDAxNTc0MDA3MTM1MDUx.TUpAaE5H-kPHeozpuPBQdQmoE0INOEO2I8AveOncBIkg.Q0pba7m7hsiNJDeTuK-g7kNLO5zYhTfBBrSRgGAdZesg.PNG.halowd/image.png?type=w966)

#### 3번 실행 시 저장폴더
![saveImg]](https://postfiles.pstatic.net/MjAxOTExMThfMTQg/MDAxNTc0MDA1NDU3MzI3.BJA-KCi25Dy1Ox7SwImuGpO0_5bCswJwQXpBoqRZXmkg.cwWO6pwqZr0LjmqQD_CxRn0_NglGsb-YVDjNpE5QmCgg.PNG.halowd/image.png?type=w966)


### 사용예제1(파일이름 지정)
```{.java}
package testArea;

import java.io.IOException;

import net.halowd.saveImg.SaveImg;

public class TestApp {
	public static void main(String[] args) {
		String imgUrl = "https://postfiles.pstatic.net/MjAxOTExMTZfMjQ2/MDAxNTczODQxNjg3NTYz.pXFjEQ3P8_uFgacA25iqWl0GnjCMQlpmbOvq4DS38AQg.6DIhw7fyF2fGYnWq-Qhx6qAqa98K4XWsAHsYg-9vrMIg.PNG.halowd/JSP.png?type=w966";
		String path = "C:/Users/LEE/Desktop/imgtest";
		String fileName = "test";

		SaveImg saveImg = new SaveImg();

		try {
			int result = saveImg.saveImgFromUrl(imgUrl, path, fileName); // 성공 시 1 리턴, 오류 시 -1 리턴
			if (result == 1) {
				System.out.println("저장된경로 : " + saveImg.getPath());
				System.out.println("저장된파일이름 : " + saveImg.getSavedFileName());
			}
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
	}
}

```

#### 3번 실행 시 콘솔 출력 내용
![saveImg]](https://postfiles.pstatic.net/MjAxOTExMThfMzEg/MDAxNTc0MDA2OTg1NDY1.GjQNrqR8xk2MXS1NrWLWS3Fs_eeOcALhK3FNjhNjU1gg.-W_9usy-OVS-2jL42DYuORXaeiVwflFix_unlttCqbog.PNG.halowd/image.png?type=w966)

#### 3번 실행 시 저장 폴더
![saveImg]](https://postfiles.pstatic.net/MjAxOTExMThfMjgx/MDAxNTc0MDA1NjIyOTY3.56mQzb0uIxpM7n4Npz-CcraS46Lxt6bNVjkM_un2Ef0g.sWcVR0QII6VLgwDrpbt4rOAWKECFrhpd_v05Hz35Kkog.PNG.halowd/image.png?type=w966)

