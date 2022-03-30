#include <windows.h>  	// use as needed for your system

#include <gl/Gl.h>

#include <gl/glut.h>

#include <stdlib.h>


float xstart, ystart, xend, r, g, h;

float yend, step, xinc, yinc, x, y;

bool check = true;

void myInit(void)
{

	glClearColor(1.0, 1.0, 1.0, 1.0);    			// set white background color
	glMatrixMode(GL_PROJECTION);
	glLoadIdentity();
	gluOrtho2D(0, 1000, 0, 600); 
}



void myDisplay(void)
{
  glClear(GL_COLOR_BUFFER_BIT);     // Clear the color buffer (background)
  glBegin(GL_LINES);
  glColor3f(r, g, h);
  glPointSize(5);
  glVertex2i(xstart, ystart);
  glVertex2i(xend, yend);
  glEnd();
  glFlush(); // Render now

}

void Keyboard(unsigned char c, int x, int y) {

  switch (c){

    case'A': 

    case 'a':

      xstart = rand() % 640;

      ystart = rand() % 480;

      xend = rand() % 640;

      yend = rand() % 480;

      r = (rand() % 9) / 8;

      g = (rand() % 9) / 8;

      h = (rand() % 9) / 8;

      break;
      


    
    
   }

  glutPostRedisplay();


}

int main(int argc, char** argv) {

	glutInit(&argc, argv);     					// initialize the toolkit

	glutInitDisplayMode(GLUT_SINGLE | GLUT_RGB); 	// set display mode 

	glutInitWindowSize(1000, 600);   				// set window size 

	glutInitWindowPosition(0, 0); 			// set window position on screen 

	glutCreateWindow("Display Graphic Primitives"); 	// open the screen window 

	glutDisplayFunc(myDisplay);   				// register redraw function 

	myInit(); 

  glutKeyboardFunc(Keyboard); 

	glutMainLoop();    		 				// go into a perpetual loop

	return 0;

}

