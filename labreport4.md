# LAB REPORT #4 Vim
---
For the lab report this week, reproduce the task from above on your own. For each numbered step (steps 4-9), 
take a screenshot, and write down exactly which keys you pressed to get to that step.

## Step 4
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/5a6fe15c-8a58-430a-991e-acc288655601)

**Keys pressed:** ssh agonzalezgomez@ieng6.ucsd.edu `<enter>`
- This new VSCode window did not have any memory of my ssh command so I typed it all completely and used enter to log in.

---
## Step 5
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/122db447-43be-4e3b-9538-492a717a8f22)

**Keys pressed:** git clone `<Ctrl+V>`, `<enter>`
- In order to clone my fork of the repository from my Github account I typed git clone and pasted my SSH url from Github using Ctrl+V and pressed enter.

---
## Step 6
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/742bb5db-479e-48aa-acf2-d4db1e25472a)

**Keys pressed:** cd lab_ `<tab>`, `<enter>`, bash `<tab>`, `<enter>`
- To run the tests I had to change my directory to be lab_7 so I typed the first few characters "cd lab_" and used the tab key to autofill the rest of the line and pressed enter. Then I typed "bash" and pressed the tab key to auto-fill the rest of the command since test.sh is the only bash file and then pressed enter. 

---
## Step 7
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/d392411e-7236-43c4-8e45-f80a8cde1f48)

**Keys pressed:** vim ListExamples.java `<enter>`
- To enter vim I typed "vim ListExamples.java" and pressed enter to enter vim in ListExamples.java


![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/57a3bd80-cd0f-4484-a50c-a5d442ef8688)
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/872e9b41-a243-4741-96fa-72e8d2df2d53)

**Keys pressed:** `j (43 times)`, `l (11 times)`, `r`, `2`, `<esc>`, `:wq`, `<enter>`
- In order to get to the line in ListExamples.java that I needed to fix I used the `j` key to move down 43 times then used the `l` key to move to the right 11 times in order to have my cursor on top of the 1 in "index1" then I pressed `r` which means replace and typed "2" to replace the 1 with a 2. Then I pressed `<esc>` to exit edit mode and type `:wq` followed by entering `<enter>` to save and exit.

---
## Step 8
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/0f116ce3-d1e4-49b0-9098-498aff882855)

**Keys pressed:** `<up>`,`<up>`,`<enter>`
- To rereun the tests I used the up arrow to access the "bash test.sh" command that was 2 up in my search history and pressed enter.

---
## Step 9
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/04402ed8-a4ee-44c8-ab4e-ecc9bcb144b3)

**Keys pressed:** git commit -m "Updated ListExamples.java" `<enter>`, git push origin main `<enter>`,
- This new VSCode window did not have any memory of commit or push commands so I typed the commit command completely then pressed enter to commit and then typed the push command completly and pressed enter to push the resulting change to my Github account.
