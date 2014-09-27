This is a glm math library port for the avr microcontroller. GLM is a very good linear algebra / math library that is used in games and has the same syntax as glsl (it's designed to mimic glsl on the PC). 

Note: most of this library is "header only", and things that are not header only are not ported yet and are not included here right now. 

The original library is unfortunately written for 32 bit processors only, so porting it is quite a task. This is by far NOT a complete port of the library. I'm just putting it here in hope that it may be useful to someone and that someone may make more features of this very good library work on AVR platform. 

Currently we have the following features working: 

- vec3, vec2 etc.. vector classes
- mat3, mat4 etc.. matrices
- quat - quaternions
- matrix, quaterion, vector multiplication
- dot, cross products

The biggest obstacle in porting this library is that it depends on STL and there is no good STL port for the AVR (at the time of this writing). The closest thing right now is the included micro-stl that "sortof" works but many features are missing. Things of particular annoyance are the library's reliance on various types being of a speciffic width (int = 32 bit). 

The best way to use this library is to put ucpp-avr into your include path and put the glm directory into your include path. Then you can include things like glm/vec3.hpp and do vector math. DO NOT include the top level GLM file because then your program will not compile since many parts of this GLM library are not ported yet! 
