# Desarrollo de la practica P2P 1.

```bash
diego@valkiria:~/uDev/github/GitP2P1$ git config --global user.email "eclixeon@gmail.com"
diego@valkiria:~/uDev/github/GitP2P1$ git config --global user.name "Diego Torres"
diego@valkiria:~/uDev/github$ mkdir GitP2P1
diego@valkiria:~/uDev/github$ git init GitP2P1
Initialized empty Git repository in /home/diego/uDev/github/GitP2P1/.git/
diego@valkiria:~/uDev/github$ cd GitP2P1/
diego@valkiria:~/uDev/github/GitP2P1$ ls
calculator.html  README.md
diego@valkiria:~/uDev/github/GitP2P1$ git add calculator.html README.md
diego@valkiria:~/uDev/github/GitP2P1$ git commit -m "x^3 Button"                         
[master (root-commit) 20f9ffd] x^3 Button
 2 files changed, 20 insertions(+)
 create mode 100644 README.md
 create mode 100644 calculator.html
diego@valkiria:~/uDev/github/GitP2P1$ git status -s
 M calculator.html
diego@valkiria:~/uDev/github/GitP2P1$ git log --online
fatal: argumento no reconocido: --online
diego@valkiria:~/uDev/github/GitP2P1$ git log --oneline
20f9ffd (HEAD -> master) x^3 Button
diego@valkiria:~/uDev/github/GitP2P1$ git diff
diff --git a/calculator.html b/calculator.html
index 19cef1e..936ca84 100644
--- a/calculator.html
+++ b/calculator.html
@@ -8,11 +8,18 @@
         var num = document.getElementById("n1");
         num.value = Math.pow(num.value, 3);
       }
+      function powFour() {
+        var num = document.getElementById("n1");
+        num.value = Math.pow(num.value, 4);
+      }
     </script>
   </head>
   <body>
     <h1>Calculadora de Diego Torres Lara</h1>
     Number:<input type="text" id="n1">
-    <p><button onclick="cube()"> x^3 </button></p>
+    <p>
+      <button onclick="cube()"> x^3 </button>
+      <button onclick="powFour()"> x^4 </button>
+    </p>
   </body>
 </html>
 diego@valkiria:~/uDev/github/GitP2P1$ git add .
 diego@valkiria:~/uDev/github/GitP2P1$  git commit -m "x^4 button"
 [master cad78ba] x^4 button
  2 files changed, 8 insertions(+), 1 deletion(-)
  create mode 100644 DevPrac_1.md
 diego@valkiria:~/uDev/github/GitP2P1$ git branch -v
 * master cad78ba x^4 button
 diego@valkiria:~/uDev/github/GitP2P1$ git add .
diego@valkiria:~/uDev/github/GitP2P1$ git commit -m "x^4 button + dev_prac.md"
[master 792ff2e] x^4 button + dev_prac.md
 1 file changed, 57 insertions(+)
diego@valkiria:~/uDev/github/GitP2P1$ git branch -v
* master 792ff2e x^4 button + dev_prac.md
diego@valkiria:~/uDev/github/GitP2P1$ git log --oneline
792ff2e (HEAD -> master) x^4 button + dev_prac.md
cad78ba x^4 button
20f9ffd x^3 Button
diego@valkiria:~/uDev/github/GitP2P1$ git checkout -b sine 20f9ffd
Se ha cambiado a una rama nueva, «sine»
diego@valkiria:~/uDev/github/GitP2P1$ git branch -v
  master 792ff2e x^4 button + dev_prac.md
* sine   20f9ffd x^3 Button
diego@valkiria:~/uDev/github/GitP2P1$ git branch -v
  master 792ff2e x^4 button + dev_prac.md
* sine   20f9ffd x^3 Button
diego@valkiria:~/uDev/github/GitP2P1$ git status -s
 M calculator.html
?? DevPrac_1.md
diego@valkiria:~/uDev/github/GitP2P1$ git log --oneline
20f9ffd (HEAD -> sine) x^3 Button
diego@valkiria:~/uDev/github/GitP2P1$ git diff
diff --git a/calculator.html b/calculator.html
index 19cef1e..2ae0d82 100644
--- a/calculator.html
+++ b/calculator.html
@@ -8,11 +8,18 @@
         var num = document.getElementById("n1");
         num.value = Math.pow(num.value, 3);
       }
+      function cube() {
+        var num = document.getElementById("n1");
+        num.value = Math.sin(num.value);
+      }
     </script>
   </head>
   <body>
     <h1>Calculadora de Diego Torres Lara</h1>
     Number:<input type="text" id="n1">
-    <p><button onclick="cube()"> x^3 </button></p>
+    <p>
+      <button onclick="cube()"> x^3 </button>
+      <button onclick="cube()"> sin(x) </button>
+    </p>
   </body>
 </html>
 diego@valkiria:~/uDev/github/GitP2P1$ git add .
diego@valkiria:~/uDev/github/GitP2P1$ git commit -m "sin(x) Button"
[sine a0f0e7b] sin(x) Button
 2 files changed, 79 insertions(+), 1 deletion(-)
 create mode 100644 DevPrac_1.md
diego@valkiria:~/uDev/github/GitP2P1$ git log --oneline --all
a0f0e7b (HEAD -> sine) sin(x) Button
792ff2e (master) x^4 button + dev_prac.md
cad78ba x^4 button
20f9ffd x^3 Button

 ```
