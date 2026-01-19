from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.boxlayout import BoxLayout

class MyApp(App):
    def build(self):
        layout = BoxLayout(orientation='vertical')
        
        # 1. متغير لتخزين اسم المستخدم (جرب تغيير الاسم هنا)
        user_name = "أحمد" 
        
        # 2. استخدام "قاعدة الشروط" (If / Else)
        if user_name == "أحمد":
            welcome_text = f"أهلاً بك يا مبرمجنا العظيم {user_name}!"
        else:
            welcome_text = "أهلاً بك أيها المستخدم الجديد."

        # 3. عرض النص المختار بناءً على الشرط
        lbl = Label(text=welcome_text)
        
        layout.add_widget(lbl)
        return layout

if __name__ == '__main__':
    MyApp().run()
    
