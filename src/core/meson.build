subdir('system')
subdir('gl')
subdir('graphics')


dependencies = [
    fmt_dep, 
    threads_dep, 
    gl_dep,
    glm_dep,
    glfw_dep,
    gleq_dep,
    glew_dep,
    imgui_dep,
    clay_dep,
    stb_dep
]

lib_inc = include_directories('.','gl','graphics','system')
dep_inc = include_directories('../')

sources = glwrapper_sources + graphics_sources + system_sources

grunge_lib = library(
    'core-framework', 
    dependencies :dependencies,
    include_directories: lib_inc,
    sources : sources
)

grunge_dep = declare_dependency(
    link_with: grunge_lib, 
    include_directories: dep_inc,
    dependencies: dependencies
)
