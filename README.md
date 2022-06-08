# digital_number_extraction

Each digit on the alarm clock is represented by a seven-segment component.

Sevent-segment displays can take on a total of 128 possible states.

We are only interested in ten of them — the digits zero to nine.

End goal is to recognize the digits on the LCD display.

**Step #1:** Localize the LCD on the complete image.
**Step #2:** Extract the LCD. Given an input edge map, find contours and look for outlines with a rectangular shape — the largest rectangular region should correspond to the LCD. A perspective transform will give a nice extraction of the LCD.
**Step #3:** Extract the digit regions. Once we have the LCD, we can focus on extracting the digits.
**Step #4:** Identify the digits. Recognizing the actual digits with OpenCV will involve dividing the digit ROI into seven segments. From there we can apply pixel counting on the thresholded image to determine if a given segment is “on” or “off”.

Refer https://pyimagesearch.com/2017/02/13/recognizing-digits-with-opencv-and-python/ for more details
