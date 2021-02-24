# [LFCS Practice Questions](https://training.linuxfoundation.org/wp-content/uploads/2019/04/LFCS-Practice-Questions-v1.0.pdf)

## Question 1
Open the file under **/home/student/textreferences/editme.txt** and complete the following tasks:
1. Move line **7777** to line **1**.
2. Remove line **7000**.
3. Replace every occurrence of the word **Earth** shown with
an uppercase E, with the word **Globe**.
4. Add a new line at the very end of the document that
contains **Auctores Varii**

### Solution
1. ``
2. `sed -i '7000d' /home/student/textreferences/editme.txt`
3. `sed -i 's/Earth/Globe/g' /home/student/textreferences/editme.txt`
4. `echo 'Auctores Varii' >> /home/student/textreferences/editme.txt`