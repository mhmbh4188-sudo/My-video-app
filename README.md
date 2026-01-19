from kivy.app import App
from kivy.uix.button import Button
from kivy.uix.label import Label
from kivy.uix.boxlayout import BoxLayout

class MyApp(App):
    def build(self):
        layout = BoxLayout(orientation='vertical')
        
        # 1. استخدام متغير لتخزين الاسم
        user_name = "المبرمج الذكي" 
        
        # 2. استخدام دالة (Label) لعرض النص على الشاشة
        self.message = Label(text=f"أهلاً بك يا {user_name}")
        
        # 3. إضافة زر يتفاعل عند الضغط عليه
        btn = Button(text="اضغط هنا للتغيير", size_hint=(1, 0.2))
        btn.bind(on_press=self.change_text) # ربط الزر بدالة التغيير
        
        layout.add_widget(self.message)
        layout.add_widget(btn)
        return layout

    # هذه دالة (Function) مهمتها تغيير النص
    def change_text(self, instance):
        self.message.text = "لقد تعلمت كيف تستخدم الدوال والمتغيرات!"

if __name__ == '__main__':
    MyApp().run()
