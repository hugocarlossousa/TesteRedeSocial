import flet as ft

def main(page: ft.Page):
    page.window_width= 450
    page.window_height= 950
    page.vertical_alignment = ft.MainAxisAlignment.CENTER
    page.horizontal_alignment = ft.MainAxisAlignment.CENTER
    page.bgcolor = ft.colors.BLACK
    
    def clicked(e):
        e.control.selected = not e.control.selected
        e.control.update()
    
    layout = ft.Container(
        bgcolor= ft.colors.GREY_100,
        width=400,
        height=650,
        border_radius= ft.border_radius.all(12),
        shadow= ft.BoxShadow(blur_radius=20, color=ft.colors.BLUE_500),
        content=ft.Column(
            controls=[
                ft.ListTile(
                    title=ft.Text(value='HigtSolutions', color=ft.colors.BLACK,weight=ft.FontWeight.BOLD),
                    subtitle=ft.Text(value='TransportationFuture', color=ft.colors.GREY_700),
                    leading=ft.Image(
                        src='https://www.ultimationinc.com/wp-content/uploads/2021/03/QM8-1030x554.png',
                        border_radius= ft.border_radius.all(35),
                                                  
                    ),
                    trailing=ft.Icon(name=ft.icons.MORE_HORIZ,color=ft.colors.GREY_700)
                
                ),
                ft.Image(
                    src='https://i.ytimg.com/vi/SAFHo0xvPBI/maxresdefault.jpg',
                    fit=ft.ImageFit.CONTAIN,
                    

                ),
                ft.Container(
                    padding=ft.padding.all(15),
                    content=ft.Column(
                        controls=[
                            ft.ResponsiveRow(
                                columns=12,
                                vertical_alignment=ft.CrossAxisAlignment.CENTER,
                                controls=[
                                    ft.IconButton(
                                        col=1,
                                        icon=ft.icons.FAVORITE_BORDER,
                                        selected_icon=ft.icons.FAVORITE,
                                        selected=False,
                                        on_click=clicked,
                                        icon_color=ft.colors.BLACK,
                                        selected_icon_color=ft.colors.RED,
                                    ),
                                    ft.Icon(
                                        col=2,
                                        name=ft.icons.CHAT_BUBBLE_OUTLINE,
                                        color=ft.colors.BLACK,
                                    ),
                                    ft.Icon(
                                        col=1,
                                        name=ft.icons.SEND,
                                        color=ft.colors.BLACK,
                                    ),
                                    ft.Container(col=6.5),
                                    ft.IconButton(
                                        col=1,
                                        icon=ft.icons.BOOKMARK_BORDER,
                                        selected_icon=ft.icons.BOOKMARK_ROUNDED,
                                        selected=False,
                                        on_click=clicked,
                                        icon_color=ft.colors.BLACK,
                                        selected_icon_color=ft.colors.BLACK,
                                    )
                                ]
                            ),
                            ft.Text(
                                spans=[
                                    ft.TextSpan(text='Curtido por... ', style=ft.TextStyle(color=ft.colors.GREY_600,size=11)),
                                    ft.TextSpan(text='HugoCarlosSousaDev', style=ft.TextStyle(color=ft.colors.BLACK,size=12, weight=ft.FontWeight.BOLD)),
                                    ft.TextSpan(text=' e ', style=ft.TextStyle(color=ft.colors.GREY_600,size=11)),
                                    ft.TextSpan(text='10010 outros.', style=ft.TextStyle(color=ft.colors.BLACK,size=12, weight=ft.FontWeight.BOLD))
                                ]
                            ),
                            ft.Text(
                                value='HS_NEWS, we have a new classifier diverter',
                                color=ft.colors.BLACK,
                                size=12
                            ),
                            ft.Text(
                                value='....35 MINUTOS ATRÁS\n\n',
                                color=ft.colors.GREY_700,
                                size=8
                            ),
                            ft.Text(
                                spans=[
                                    ft.TextSpan(text='HugoCarlosSousaDev', style=ft.TextStyle(color=ft.colors.BLACK,size=12, weight=ft.FontWeight.BOLD)),
                                    ft.TextSpan(text=' Wow!!!!!!! this is so cool @HigtSolutions', style=ft.TextStyle(color=ft.colors.GREY_600,size=11)),
                                    
                                ]
                            ),
                            ft.Text(
                                value=' Ver os outros 10009 comentário',
                                color=ft.colors.GREY_700,
                                size=8
                            ),
                            ft.TextField(
                                hint_text='Adicione um comentário',
                                hint_style=ft.TextStyle(color=ft.colors.GREY_600,size=9),
                                border= ft.InputBorder.NONE,
                                color=ft.colors.BLACK
                            )
                        ]   
                    )
                    
                )
            ]
        )
        
    )
    
    page.add(layout)
    
    
if __name__ == '__main__':
    ft.app(target=main)
    
    
