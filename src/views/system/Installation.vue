<template>
  <a-row align="middle" class="h-screen" justify="center" type="flex">
    <a-col :lg="16" :md="20" :sm="20" :xl="12" :xs="23" :xxl="8">
      <div class="card-container animated fadeIn">
        <a-card :bordered="false" style="box-shadow: rgba(99, 99, 99, 0.2) 0 2px 8px 0">
          <div class="halo-logo">
            <img
              alt="Sonic Logo"
              src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4KPCEtLSBHZW5lcmF0b3I6IEFkb2JlIElsbHVzdHJhdG9yIDI3LjAuMCwgU1ZHIEV4cG9ydCBQbHVnLUluIC4gU1ZHIFZlcnNpb246IDYuMDAgQnVpbGQgMCkgIC0tPgo8c3ZnIHZlcnNpb249IjEuMSIgaWQ9Il/lm77lsYJfMiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgeD0iMHB4IiB5PSIwcHgiCgkgdmlld0JveD0iMCAwIDYxMC42IDY5OS41IiBzdHlsZT0iZW5hYmxlLWJhY2tncm91bmQ6bmV3IDAgMCA2MTAuNiA2OTkuNTsiIHhtbDpzcGFjZT0icHJlc2VydmUiPgo8c3R5bGUgdHlwZT0idGV4dC9jc3MiPgoJLnN0MHtmaWxsOiMyMTE4MTU7fQoJLnN0MXtmaWxsOnVybCgjU1ZHSURfMV8pO30KCS5zdDJ7ZmlsbDp1cmwoI1NWR0lEXzAwMDAwMDEzMTg5Mzk1MDQ0MTU2MDAxMzQwMDAwMDEyNjAxNTA0NzQwMTEwMzM4OTY0Xyk7fQoJLnN0M3tmaWxsOnVybCgjU1ZHSURfMDAwMDAwNzU4NzEyOTU3NTMzMTE5MzU3NDAwMDAwMDQ3NTY0NzU0NDExODM5Njg5NTVfKTt9Cgkuc3Q0e2ZpbGw6dXJsKCNTVkdJRF8wMDAwMDA5NDYxMjE4MzM3MDM2OTUzNjIzMDAwMDAwNDM3MzYzODExNjg0NTQwNjY1MF8pO30KPC9zdHlsZT4KPGcgaWQ9Il/lm77lsYJfMS0yIj4KCTxnPgoJCTxnPgoJCQk8cGF0aCBjbGFzcz0ic3QwIiBkPSJNNzksNjYwLjdjMC45LTYtMC40LTEwLjQtMy44LTEzLjRzLTEwLjEtNi4yLTIwLTkuOUMzNy43LDYzMS43LDI0LjcsNjI0LjksMTYsNjE3CgkJCQljLTguNy03LjktMTIuMS0xNy44LTEwLjMtMjkuOGMxLjgtMTIsOC4xLTIxLjUsMTktMjguNWMxMC45LTcsMjQtMTAuNCwzOS4zLTEwLjRjMTYuNywwLDI5LjgsNCwzOS4yLDEyYzkuNSw4LDEzLDE5LDEwLjYsMzMKCQkJCWwtMC4yLDAuNkg4MC41YzAuOC01LjgtMC43LTEwLjUtNC41LTE0Yy0zLjgtMy42LTkuMS01LjMtMTUuOS01LjNjLTUsMC05LjUsMS4yLTEzLjQsMy42cy02LjIsNS40LTYuOCw4LjkKCQkJCWMtMC44LDUuNSwwLjcsOS41LDQuNSwxMi4yczEyLDYuMiwyNC40LDEwLjZjMTUuOSw1LjIsMjcuNywxMS43LDM1LjQsMTkuN2M3LjcsNy45LDEwLjcsMTguMyw4LjgsMzEKCQkJCWMtMS45LDEyLjYtOC4zLDIyLjItMTguOSwyOC45Yy0xMC43LDYuNy0yMy45LDEwLTM5LjYsMTBzLTI5LjgtMy43LTQxLTExcy0xNS40LTE4LjctMTIuOC0zNGwwLjItMC42aDMzLjEKCQkJCWMtMS4xLDcuMiwwLjgsMTIuMiw1LjksMTUuMWM1LjEsMi45LDExLjIsNC4zLDE4LjUsNC4zYzUsMCw5LjUtMS4yLDEzLjYtMy42Uzc4LjQsNjY0LjMsNzksNjYwLjdMNzksNjYwLjd6Ii8+CgkJCTxwYXRoIGNsYXNzPSJzdDAiIGQ9Ik0yNTQuMSw2MzcuMWMtMi45LDE4LjgtMTAuOSwzMy45LTIzLjksNDUuM3MtMjguOSwxNy00Ny42LDE3cy0zMS45LTUuOS00Mi4xLTE3LjhzLTEzLjktMjYuNy0xMS4xLTQ0LjUKCQkJCWwzLjktMjYuNGMyLjgtMTguNywxMC43LTMzLjgsMjMuOS00NS4yYzEzLjEtMTEuNCwyOS4xLTE3LjIsNDgtMTcuMmMxNy44LDAsMzEuNyw1LjksNDEuOCwxNy44czEzLjgsMjYuNywxMS4yLDQ0LjVMMjU0LjEsNjM3LjEKCQkJCUwyNTQuMSw2MzcuMXogTTIyNCw2MTAuNWMxLjYtMTAuOSwwLjUtMTkuNi0zLjQtMjYuMXMtMTAuNC05LjgtMTkuNS05LjhzLTE2LjQsMy40LTIyLjQsMTAuMXMtOS45LDE1LjMtMTEuNCwyNS44bC0zLjksMjYuNgoJCQkJYy0xLjcsMTEtMC42LDE5LjgsMy40LDI2LjNjMy45LDYuNSwxMC41LDkuOCwxOS44LDkuOGM4LjYsMCwxNi0zLjQsMjItMTAuMmM2LjEtNi44LDkuOS0xNS40LDExLjYtMjUuOUwyMjQsNjEwLjVMMjI0LDYxMC41eiIvPgoJCQk8cGF0aCBjbGFzcz0ic3QwIiBkPSJNMzg4LjMsNjk3LjRoLTM0bC00MC05Mi40bC0wLjYsMC4xbC0xMy43LDkyLjNoLTM0LjFsMjItMTQ2LjloMzQuMWw0MCw5Mi4zbDAuNi0wLjFsMTMuOC05Mi4yaDM0CgkJCQlMMzg4LjMsNjk3LjRMMzg4LjMsNjk3LjR6Ii8+CgkJCTxwYXRoIGNsYXNzPSJzdDAiIGQ9Ik00NTIsNjk3LjRoLTM0bDIyLTE0Ni45aDM0TDQ1Miw2OTcuNHoiLz4KCQkJPHBhdGggY2xhc3M9InN0MCIgZD0iTTYwMS44LDY0Ny44bDAuMiwwLjZjLTIuNCwxNy40LTksMzAuMy0xOS44LDM4LjZjLTEwLjgsOC4zLTI1LjMsMTIuNS00My40LDEyLjVzLTMxLjEtNS42LTQwLjgtMTYuOAoJCQkJcy0xMy4yLTI1LjctMTAuNS00My40bDQuNi0zMC43YzIuOC0xOC42LDEwLjItMzMuMiwyMi4zLTQ0YzEyLjEtMTAuOCwyNy0xNi4yLDQ0LjYtMTYuMnMzMS41LDQuNCw0MC43LDEzLjEKCQkJCWM5LjIsOC43LDEyLjQsMjEuMyw5LjcsMzcuN2wtMC4zLDAuNmgtMzMuM2MxLjMtOS4zLDAuNC0xNS45LTIuNy0xOS42cy05LjItNS42LTE4LjEtNS42Yy03LjMsMC0xMy42LDMuMS0xOC45LDkuMwoJCQkJYy01LjIsNi4yLTguNiwxNC40LTEwLjEsMjQuNWwtNC42LDMwLjljLTEuNiwxMC42LTAuNiwxOSwzLDI1YzMuNiw2LDkuNiw5LDE4LjEsOWM3LjUsMCwxMy4zLTIsMTcuNS02YzQuMi00LDctMTAuNSw4LjQtMTkuNQoJCQkJTDYwMS44LDY0Ny44TDYwMS44LDY0Ny44eiIvPgoJCTwvZz4KCTwvZz4KCTxnPgoJCQoJCQk8bGluZWFyR3JhZGllbnQgaWQ9IlNWR0lEXzFfIiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSIgeDE9Ii0xMzg5LjcwNCIgeTE9IjE0OTAuMzk4MyIgeDI9Ii0xMTk1LjQzODciIHkyPSIxODA3LjQyMDgiIGdyYWRpZW50VHJhbnNmb3JtPSJtYXRyaXgoMC45NzI0IDAuMjMzNCAwLjIzMzQgLTAuOTcyNCAxMTc3LjIxMzYgMjE1Ny45MDE0KSI+CgkJCTxzdG9wICBvZmZzZXQ9IjAiIHN0eWxlPSJzdG9wLWNvbG9yOiMwMDQ2QTUiLz4KCQkJPHN0b3AgIG9mZnNldD0iMSIgc3R5bGU9InN0b3AtY29sb3I6Izc4RjBGRiIvPgoJCTwvbGluZWFyR3JhZGllbnQ+CgkJPHBhdGggY2xhc3M9InN0MSIgZD0iTTM5NS43LDM2MmMtMy4xLDEyLjktOC4zLDI0LjctMTUuMSwzNS4yYy0xMC42LDE2LjQtMjUuMiwyOS41LTQyLjEsMzguNWMtMjMuNSwxMi41LTUxLjYsMTYuOC03OS41LDEwCgkJCWMtMjgtNi43LTUxLTIzLjItNjYuMy00NS4xYy0xMS0xNS42LTE4LTM0LTIwLTUzLjRjMTEuOC01LjYsMjQuMi05LjksMzcuMS0xMi43YzkuMS0yLDE4LjMsMy44LDIwLjMsMTIuOQoJCQljNC41LDIwLjYsMjAuMywzNy45LDQyLjIsNDMuMWMyNy4zLDYuNiw1NC44LTcuOSw2NS40LTMyLjljMS4yLTIuOSwyLjItNS45LDMtOXMxLjItNi4yLDEuNC05LjNjMS45LTI3LjEtMTYtNTIuNS00My4zLTU5CgkJCWMtMjgtNi43LTUxLTIzLjItNjYuMy00NS4xYy0xMS0xNS42LTE4LTM0LTIwLTUzLjRjLTEuMy0xMi41LTAuNi0yNS40LDIuNS0zOC4zYzMuMS0xMi45LDguMy0yNC43LDE1LjEtMzUuMwoJCQljMTAuNi0xNi40LDI1LjItMjkuNSw0Mi4xLTM4LjVjMjMuNS0xMi41LDUxLjYtMTYuOCw3OS41LTEwLjFzNTEsMjMuMiw2Ni4zLDQ1LjFjMTEsMTUuNiwxOCwzNCwyMCw1My40CgkJCWMtMTEuOCw1LjYtMjQuMiw5LjktMzcuMSwxMi43Yy05LjEsMi0xOC4zLTMuOC0yMC4zLTEyLjljLTQuNS0yMC42LTIwLjMtMzcuOC00Mi4yLTQzLjFjLTI3LjMtNi42LTU0LjgsNy45LTY1LjQsMzIuOQoJCQljLTEuMiwyLjktMi4yLDUuOS0zLDljLTAuOCwzLjEtMS4yLDYuMi0xLjQsOS4zYy0xLjksMjcuMSwxNiw1Mi41LDQzLjMsNTljMjgsNi43LDUxLDIzLjIsNjYuMyw0NS4xYzExLDE1LjYsMTgsMzQsMjAsNTMuNAoJCQlDMzk5LjUsMzM2LjIsMzk4LjgsMzQ5LjEsMzk1LjcsMzYyTDM5NS43LDM2MnoiLz4KCQkKCQkJPGxpbmVhckdyYWRpZW50IGlkPSJTVkdJRF8wMDAwMDA2NTA2MjEzMzUyNjQ4MjE2MDM4MDAwMDAwMDc3NjI0NTM5NDgyODQ0MzA1MF8iIGdyYWRpZW50VW5pdHM9InVzZXJTcGFjZU9uVXNlIiB4MT0iLTE0MTkuMzkzMSIgeTE9IjE2MTIuMTczMyIgeDI9Ii0xMjQxLjY0NDciIHkyPSIxOTAyLjIzMDciIGdyYWRpZW50VHJhbnNmb3JtPSJtYXRyaXgoMC45NzI0IDAuMjMzNCAwLjIzMzQgLTAuOTcyNCAxMTc3LjIxMzYgMjE1Ny45MDE0KSI+CgkJCTxzdG9wICBvZmZzZXQ9IjAiIHN0eWxlPSJzdG9wLWNvbG9yOiMwMDQ2QTUiLz4KCQkJPHN0b3AgIG9mZnNldD0iMSIgc3R5bGU9InN0b3AtY29sb3I6Izc4RjBGRiIvPgoJCTwvbGluZWFyR3JhZGllbnQ+CgkJPHBhdGggc3R5bGU9ImZpbGw6dXJsKCNTVkdJRF8wMDAwMDA2NTA2MjEzMzUyNjQ4MjE2MDM4MDAwMDAwMDc3NjI0NTM5NDgyODQ0MzA1MF8pOyIgZD0iTTQ4MC4yLDEyOS43CgkJCWMtMTIuNiwxMS42LTI2LjksMjEuMi00Mi4zLDI4LjZjLTItMTkuNC05LTM3LjctMjAtNTMuNGMtMTUuMy0yMS44LTM4LjMtMzguNC02Ni4zLTQ1LjFjLTI4LTYuNy01Ni0yLjQtNzkuNSwxMC4xCgkJCWMtMTYuOSw4LjktMzEuNSwyMi4xLTQyLjEsMzguNWMtNi44LDEwLjUtMTIsMjIuNC0xNS4xLDM1LjNjLTMuMSwxMi45LTMuOSwyNS44LTIuNSwzOC4zYzIsMTkuNCw5LjEsMzcuOCwyMCw1My40CgkJCWMxNS4zLDIxLjgsMzguMywzOC40LDY2LjMsNDUuMWMtMjEuOS01LjItNDMuOCwyLjktNTcuMSwxOS4yYy01LjksNy4yLTE2LjcsOC4yLTIzLjksMi4zYy0xMC4yLTguMy0xOS4zLTE3LjgtMjcuMy0yOC4xCgkJCWMtMTIuNy0xNi41LTIyLjMtMzUuMy0yOC4zLTU1LjRjLTguMi0yNy43LTkuNS01Ny45LTIuMy04OGM3LjItMzAuMSwyMi4xLTU2LjQsNDItNzcuNGMxNC40LTE1LjIsMzEuNS0yNy41LDUwLjMtMzYuNQoJCQljMTcuNS04LjQsMzYuNS0xMy43LDU2LjItMTUuN2MxOC41LTEuOCwzNy41LTAuNyw1Ni42LDMuOXMzNi42LDEyLjIsNTIuMiwyMi4yYzE2LjcsMTAuNywzMS4xLDI0LjEsNDMsMzkuNQoJCQljMTAuNCwxMy42LDE4LjgsMjguNiwyNC43LDQ0LjdDNDg3LjEsMTE3LjcsNDg1LjMsMTI1LDQ4MC4yLDEyOS43TDQ4MC4yLDEyOS43eiIvPgoJCQoJCQk8bGluZWFyR3JhZGllbnQgaWQ9IlNWR0lEXzAwMDAwMDM0MDY0MjYzNzk4MDI4MTA2OTMwMDAwMDA5NDk0ODE0MjMzMTE0OTU4MjIzXyIgZ3JhZGllbnRVbml0cz0idXNlclNwYWNlT25Vc2UiIHgxPSItMTM0My41MTE1IiB5MT0iMTM5NS41NzU2IiB4Mj0iLTExNjUuNzUyNiIgeTI9IjE2ODUuNjUwMSIgZ3JhZGllbnRUcmFuc2Zvcm09Im1hdHJpeCgwLjk3MjQgMC4yMzM0IDAuMjMzNCAtMC45NzI0IDExNzcuMjEzNiAyMTU3LjkwMTQpIj4KCQkJPHN0b3AgIG9mZnNldD0iMCIgc3R5bGU9InN0b3AtY29sb3I6IzAwNDZBNSIvPgoJCQk8c3RvcCAgb2Zmc2V0PSIxIiBzdHlsZT0ic3RvcC1jb2xvcjojNzhGMEZGIi8+CgkJPC9saW5lYXJHcmFkaWVudD4KCQk8cGF0aCBzdHlsZT0iZmlsbDp1cmwoI1NWR0lEXzAwMDAwMDM0MDY0MjYzNzk4MDI4MTA2OTMwMDAwMDA5NDk0ODE0MjMzMTE0OTU4MjIzXyk7IiBkPSJNNDUwLjgsMzc1LjIKCQkJYy03LjIsMzAuMS0yMi4xLDU2LjQtNDIsNzcuNGMtMTQuNCwxNS4yLTMxLjUsMjcuNS01MC4zLDM2LjVjLTE3LjUsOC40LTM2LjUsMTMuOC01Ni4yLDE1LjdjLTE4LjUsMS44LTM3LjUsMC43LTU2LjYtMy45CgkJCXMtMzYuNi0xMi4yLTUyLjItMjIuMmMtMTYuNy0xMC43LTMxLjEtMjQuMS00My0zOS41Yy0xMC40LTEzLjUtMTguOC0yOC42LTI0LjctNDQuN2MtMi40LTYuNS0wLjctMTMuOSw0LjUtMTguNgoJCQljMTIuNi0xMS42LDI2LjktMjEuMiw0Mi4zLTI4LjZjMiwxOS40LDkuMSwzNy44LDIwLDUzLjRjMTUuMywyMS44LDM4LjMsMzguNCw2Ni4zLDQ1LjFjMjgsNi43LDU2LDIuNCw3OS41LTEwCgkJCWMxNi45LTksMzEuNS0yMi4xLDQyLjEtMzguNWM2LjgtMTAuNSwxMi0yMi40LDE1LjEtMzUuMmMzLjEtMTIuOSwzLjktMjUuOCwyLjUtMzguM2MtMi0xOS40LTktMzcuNy0yMC01My40CgkJCWMtMTUuMy0yMS44LTM4LjMtMzguNC02Ni4zLTQ1LjFjMjEuOSw1LjIsNDMuOC0yLjksNTcuMS0xOS4zYzUuOS03LjIsMTYuNy04LjIsMjMuOS0yLjNjMTAuMiw4LjMsMTkuMywxNy44LDI3LjMsMjguMQoJCQljMTIuNywxNi41LDIyLjMsMzUuMywyOC4zLDU1LjRDNDU2LjgsMzE0LjksNDU4LjEsMzQ1LjEsNDUwLjgsMzc1LjJMNDUwLjgsMzc1LjJ6Ii8+CgkJCgkJCTxsaW5lYXJHcmFkaWVudCBpZD0iU1ZHSURfMDAwMDAxMDYxMDcwMDAyOTI3NjUzMTgxNDAwMDAwMDgwMTk3MTM5MjY5MDM0Nzc0MTBfIiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSIgeDE9Ii0xMzQ1LjgzNTkiIHkxPSIxNTYxLjk2NjgiIHgyPSItMTIzOS4yOTIxIiB5Mj0iMTczNS44NDMzIiBncmFkaWVudFRyYW5zZm9ybT0ibWF0cml4KDAuOTcyNCAwLjIzMzQgMC4yMzM0IC0wLjk3MjQgMTE3Ny4yMTM2IDIxNTcuOTAxNCkiPgoJCQk8c3RvcCAgb2Zmc2V0PSIwIiBzdHlsZT0ic3RvcC1jb2xvcjojMDA0NkE1Ii8+CgkJCTxzdG9wICBvZmZzZXQ9IjEiIHN0eWxlPSJzdG9wLWNvbG9yOiM3OEYwRkYiLz4KCQk8L2xpbmVhckdyYWRpZW50PgoJCTxwYXRoIHN0eWxlPSJmaWxsOnVybCgjU1ZHSURfMDAwMDAxMDYxMDcwMDAyOTI3NjUzMTgxNDAwMDAwMDgwMTk3MTM5MjY5MDM0Nzc0MTBfKTsiIGQ9Ik0zMzIsMTQxLjVjLTE1LjgtMy44LTMxLjcsNS45LTM1LjUsMjEuOAoJCQljLTMuOCwxNS44LDUuOSwzMS43LDIxLjgsMzUuNWMxNS44LDMuOCwzMS43LTUuOSwzNS41LTIxLjhDMzU3LjYsMTYxLjIsMzQ3LjgsMTQ1LjMsMzMyLDE0MS41TDMzMiwxNDEuNXogTTI5Mi4zLDMwNi45CgkJCWMtMTUuOC0zLjgtMzEuNyw2LTM1LjUsMjEuOGMtMy44LDE1LjgsNS45LDMxLjcsMjEuOCwzNS41YzE1LjgsMy44LDMxLjctNiwzNS41LTIxLjhDMzE3LjksMzI2LjYsMzA4LjEsMzEwLjcsMjkyLjMsMzA2Ljl6Ii8+Cgk8L2c+CjwvZz4KPC9zdmc+Cg=="
            />
            <span>安装向导</span>
          </div>
          <a-alert :message="`欢迎使用 Sonic`" show-icon type="success" />
          <!-- Blogger info -->
          <div class="mt-5 mb-5">
            <a-radio-group v-model="installationMode">
              <a-radio-button value="new"> 全新安装</a-radio-button>
              <a-radio-button value="import"> 数据导入</a-radio-button>
            </a-radio-group>
          </div>
          <a-form-model
            v-show="isInstallMode"
            ref="installationForm"
            :model="form.model"
            :rules="form.rules"
            class="installationForm animated fadeIn"
            layout="horizontal"
          >
            <a-divider dashed orientation="left"> 管理员信息</a-divider>
            <a-form-model-item prop="username">
              <a-input v-model="form.model.username" placeholder="用户名">
                <a-icon slot="prefix" style="color: rgba(0, 0, 0, 0.25)" type="user" />
              </a-input>
            </a-form-model-item>
            <a-form-model-item prop="username">
              <a-input v-model="form.model.nickname" placeholder="用户昵称">
                <a-icon slot="prefix" style="color: rgba(0, 0, 0, 0.25)" type="user" />
              </a-input>
            </a-form-model-item>
            <a-form-model-item prop="email">
              <a-input v-model="form.model.email" placeholder="用户邮箱">
                <a-icon slot="prefix" style="color: rgba(0, 0, 0, 0.25)" type="mail" />
              </a-input>
            </a-form-model-item>
            <a-form-model-item prop="password">
              <a-input v-model="form.model.password" placeholder="登录密码（8-100位）" type="password">
                <a-icon slot="prefix" style="color: rgba(0, 0, 0, 0.25)" type="lock" />
              </a-input>
            </a-form-model-item>
            <a-form-model-item prop="confirmPassword">
              <a-input v-model="form.model.confirmPassword" placeholder="确认登录密码" type="password">
                <a-icon slot="prefix" style="color: rgba(0, 0, 0, 0.25)" type="lock" />
              </a-input>
            </a-form-model-item>
            <a-divider dashed orientation="left"> 站点信息</a-divider>
            <a-form-model-item prop="url">
              <a-input v-model="form.model.url" placeholder="博客地址">
                <a-icon slot="prefix" style="color: rgba(0, 0, 0, 0.25)" type="link" />
              </a-input>
            </a-form-model-item>
            <a-form-model-item prop="title">
              <a-input v-model="form.model.title" placeholder="博客标题">
                <a-icon slot="prefix" style="color: rgba(0, 0, 0, 0.25)" type="book" />
              </a-input>
            </a-form-model-item>
          </a-form-model>

          <!-- Data migration -->
          <div v-show="isImportMode" class="animated fadeIn">
            <FilePondUpload
              ref="upload"
              :accepts="['application/json']"
              :multiple="false"
              :uploadHandler="onImportUpload"
              label="拖拽或点击选择数据文件<br>请确认是否为 Sonic 后台导出的文件。"
              name="file"
            ></FilePondUpload>
          </div>

          <div class="mt-8">
            <ReactiveButton
              v-if="isInstallMode"
              :errored="form.installErrored"
              :loading="form.installing"
              block
              erroredText="安装失败"
              icon="check"
              loadedText="安装成功"
              size="large"
              text="安装"
              type="primary"
              @callback="handleInstallCallback"
              @click="handleInstall"
            ></ReactiveButton>
            <ReactiveButton
              v-if="isImportMode"
              :errored="form.importErrored"
              :loading="form.importing"
              block
              erroredText="导入失败"
              icon="import"
              loadedText="导入成功"
              size="large"
              text="导入"
              type="primary"
              @callback="handleImportCallback"
              @click="handleImport"
            ></ReactiveButton>
          </div>
        </a-card>
      </div>
    </a-col>
  </a-row>
</template>

<script>
import apiClient from '@/utils/api-client'
import { mapActions } from 'vuex'

export default {
  data() {
    const confirmPasswordValidate = (rule, value, callback) => {
      if (value !== this.form.model.password) {
        callback(new Error('确认密码与所输入的密码不一致'))
      } else {
        callback()
      }
    }
    return {
      installationMode: 'new', // new or import
      form: {
        model: {},
        rules: {
          username: [
            { required: true, message: '* 用户名不能为空', trigger: ['change'] },
            { max: 50, message: '* 用户名的字符长度不能超过 50', trigger: ['change'] }
          ],
          nickname: [
            { required: true, message: '* 用户昵称不能为空', trigger: ['change'] },
            { max: 255, message: '* 用户昵称的字符长度不能超过 255', trigger: ['change'] }
          ],
          email: [
            { required: true, message: '* 电子邮件地址不能为空', trigger: ['change'] },
            { max: 127, message: '* 电子邮件地址的字符长度不能超过 127', trigger: ['change'] },
            {
              pattern: /\w[-\w.+]*@([A-Za-z0-9][-A-Za-z0-9]+\.)+[A-Za-z]{2,14}/g,
              message: '* 电子邮件地址的格式不正确',
              trigger: ['change']
            }
          ],
          password: [
            { required: true, message: '* 密码不能为空', trigger: ['change'] },
            { min: 8, max: 100, message: '* 密码的字符长度必须在 8 - 100 之间', trigger: ['change'] }
          ],
          confirmPassword: [
            { required: true, message: '* 确认密码不能为空', trigger: ['change'] },
            { validator: confirmPasswordValidate, trigger: ['change'] }
          ],
          url: [{ required: true, message: '* 博客地址不能为空', trigger: ['change'] }],
          title: [{ required: true, message: '* 博客标题不能为空', trigger: ['change'] }]
        },
        installing: false,
        installErrored: false,

        importing: false,
        importErrored: false,
        importData: null
      }
    }
  },
  beforeMount() {
    this.$set(this.form.model, 'url', window.location.protocol + '//' + window.location.host)
  },
  computed: {
    isInstallMode() {
      return this.installationMode === 'new'
    },
    isImportMode() {
      return this.installationMode === 'import'
    }
  },
  methods: {
    ...mapActions(['installCleanToken', 'fetchIsInstalled']),
    handleInstall() {
      this.$refs.installationForm.validate(valid => {
        if (valid) {
          this.form.installing = true
          this.installCleanToken(this.form.model)
            .then(response => {
              this.$log.debug('Installation response', response)
            })
            .catch(() => {
              this.form.installErrored = true
            })
            .finally(() => {
              setTimeout(() => {
                this.form.installing = false
              }, 400)
              this.fetchIsInstalled()
            })
        }
      })
    },
    handleInstallCallback() {
      if (this.form.installErrored) {
        this.form.installErrored = false
      } else {
        this.$message.success('安装成功！')
        this.$router.push({ name: 'Login' })
      }
    },
    onImportUpload(data) {
      this.$log.debug('Selected data', data)
      this.form.importData = data
      return new Promise(resolve => {
        this.$log.debug('Handle uploading')
        resolve()
      })
    },
    handleImport() {
      if (!this.form.importData) {
        this.$message.warning('请先上传数据文件！')
        return
      }
      this.form.importing = true
      apiClient.migration
        .migrate(this.form.importData)
        .then(() => {
          this.$log.debug('Migrated successfully')
        })
        .catch(() => {
          this.form.importErrored = true
        })
        .finally(() => {
          setTimeout(() => {
            this.form.importing = false
          }, 400)
          this.fetchIsInstalled()
        })
    },
    handleImportCallback() {
      if (this.form.importErrored) {
        this.form.importErrored = false
      } else {
        this.$message.success('导入成功！')
        this.$router.replace({ name: 'Login' })
      }
    }
  }
}
</script>
<style lang="less" scoped>
::v-deep .installationForm {
  .ant-divider {
    .ant-divider-inner-text {
      padding-left: 0;
    }

    &::before {
      width: 0;
    }
  }
}
</style>
