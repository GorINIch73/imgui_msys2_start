# imgui_msys2_start
хелло ворд для имгуи под винду мсис2

Откройте MSYS2 MinGW x64 и выполните:
pacman -Syu                          # Обновление системы
pacman -S --needed base-devel        # Базовые инструменты разработки
pacman -S mingw-w64-x86_64-toolchain # Компилятор MinGW-w64
pacman -S mingw-w64-x86_64-cmake     # CMake для MinGW
pacman -S mingw-w64-x86_64-glfw      # GLFW (оконная система для ImGui)


Сборка проекта: (докачает imgui)
mkdir build && cd build
cmake -G "MinGW Makefiles" ..
cmake --build . 
./hello_imgui.exe

некоторык dll нужно положить руками

для релиза
cmake -G "MinGW Makefiles" -DCMAKE_BUILD_TYPE=Release ..

