project('glew-meson-example', 'cpp',
  version : '0.1',
  default_options : ['warning_level=3',
                     'cpp_std=c++14'])

dependencies=[]

glfw3_subproj = subproject('glfw')
glfw3_dep = glfw3_subproj.get_variable('glfw_dep')

dependencies += glfw3_dep

glew_subproj = subproject('glew')
glew_dep = glew_subproj.get_variable('glew_dep')

dependencies += glew_dep

exe = executable('glew_meson_example', 'glew_meson_example.cpp',
  install : true, dependencies: dependencies)

test('basic', exe)
