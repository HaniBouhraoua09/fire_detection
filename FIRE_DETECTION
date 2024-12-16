import cv2
from playsound import playsound

camera = cv2.VideoCapture(0)

Fire_Algorithm = "fire_detection.xml"

Fire_detection = cv2.CascadeClassifier(Fire_Algorithm)

while True :
    access , frame = camera.read()

    Fire_detected = Fire_detection.detectMultiScale(frame , 1.2 , 5)
    print(Fire_detected)

    for x , y , height , width in Fire_detected :
        cv2.rectangle(frame ,(x + 150 , y + 150) ,(width  , height) , (0,0,255) , thickness = 2)
        bonding_nox = frame[x : x + height , y : y + width]
        print("Fire is detected !!")
        playsound("audio.mp3")
          
    
    cv2.imshow("photo" , frame)
    if cv2.waitKey(1) == ord('q') :
        break
