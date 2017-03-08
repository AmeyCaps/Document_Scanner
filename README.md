# Document_Scanner
Document scanner using OpenCV (3.2.0) and Python (2.7.12).

A very thanks to author of article http://www.pyimagesearch.com/2014/09/01/build-kick-ass-mobile-document-scanner-just-5-minutes/ for great explanations to learn from.  

Image is - 

1.Converted to greayscale - 

 ```Python 
 grey = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
 ```
2.Blurred to smooth - 

```Python
blurr = cv2.GaussianBlur(grey, (5,5),0)
```
3.Now we find edges in blurred image- 

```Python
edge = cv2.Canny(blurr, 0, 50)
```
![contour](https://cloud.githubusercontent.com/assets/9251814/23702919/5bf364dc-0423-11e7-9cb9-fe4bbbe6ddd6.jpg)

4.Next is to find contours-

```Python
_, contours, _ = cv2.findContours(edge, cv2.RETR_LIST, cv2.CHAIN_APPROX_SIMPLE)
```
5.After contour approximation -

![contour](https://cloud.githubusercontent.com/assets/9251814/23703776/9efe646c-0427-11e7-901a-a2d648b9e5c3.jpg)

6.Image after prespective transform (This particular part is very well explained in article at [pyimagesearch]( http://www.pyimagesearch.com/2014/09/01/build-kick-ass-mobile-document-scanner-just-5-minutes/))- 

![scanned](https://cloud.githubusercontent.com/assets/9251814/23703883/2fb9b308-0428-11e7-9aac-1e7d24059c6c.jpg)





 `
