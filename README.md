# 2022graphics1
week02

 1. 下載範例 https://jsyeh.org/3dcg10

   data.zip windows.zip glut32.dll

2. windows.zip =解壓=> 下載\windows\Shapes.exe

   data.zip =解壓=> 下載\windows\data\模型

   glut32.dll =複製=> 下載\windows\glut32.dll

3. 跑 Shapes.exe 看範例, 試試看

   左可按右鍵選單: 大頂點、很多顏色

   右可按右鍵選單: POINT....POLYGON 



1. 上週的安裝 Git for Windows
2. 上週的 Git Bash: cd desktop, git clone 你的網址 cd 2022graphics



3. 上週的安裝 freeglut, 記得改檔名 lib\libglut32.a

4. 在 CodeBlocks File-Open week01_GLUT專案,跑!
/*

 * GLUT Shapes Demo

 *

 * Written by Nigel Stewart November 2003

 *

 * This program is test harness for the sphere, cone

 * and torus shapes in GLUT.

 *

 * Spinning wireframe and smooth shaded shapes are

 * displayed until the ESC or q key is pressed.  The

 * number of geometry stacks and slices can be adjusted

 * using the + and - keys.

 */
 
 ```c++
#include <GL/glut.h>
/* GLUT callback Handlers */
static void display(void)
{
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT);
    glColor3f(1,1,0);
    glutSolidTeapot(0.3);
    glutSwapBuffers();
}
int main(int argc, char *argv[])
{
    glutInit(&argc, argv);
    glutInitDisplayMode(GLUT_DOUBLE | GLUT_DEPTH);
    glutCreateWindow("第02週的程式喔!");
    glutDisplayFunc(display);
    glutMainLoop();
}
```
```c++
#include <GL./glut.h>
void display()
{
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT );
    glColor3f(1,1,0);
    //glutSolidTeapot(0.3);
    glBegin(GL_POLYGON);
        glColor3f(1,0,0);
        glVertex2f(-1, -1);
        glColor3f(0,1,0);
        glVertex2f(+1, -1);
        glColor3f(0,0,1);
        glVertex2f(0, +1);
    glEnd();
    glutSwapBuffers();
}
int main(int argc, char** argv)
{
    glutInit(&argc, argv);
    glutInitDisplayMode( GLUT_DOUBLE | GLUT_DEPTH );
    glutCreateWindow("第二週的程式喔!");
    glutDisplayFunc(display);
    glutMainLoop();
}
```


