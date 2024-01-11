```python
from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.gridlayout import GridLayout
from kivy.uix.textinput import TextInput
from kivy.uix.button import Button

class MyGridLayout(GridLayout):
    # initialize infinite keywords
    def __init__(self, **kwargs):
        # call grid layout constructor
        super(MyGridLayout, self).__init__(**kwargs)

        # set columns
        self.cols = 1

        # create a second gridlayout
        self.top_grid = GridLayout()
        self.top_grid.cols = 2

        
        # add widgets
        self.top_grid.add_widget(Label(text="Name: "))
        self.name = TextInput(multiline=False) # input box - multiline=False means you can only enter in 1 lines
        self.top_grid.add_widget(self.name)

        self.top_grid.add_widget(Label(text="Favorite Pizza: "))
        self.pizza = TextInput(multiline=False) # input box
        self.top_grid.add_widget(self.pizza)

        self.top_grid.add_widget(Label(text="Favorite Color: "))
        self.color = TextInput(multiline=False) # input box
        self.top_grid.add_widget(self.color)

        # add thje new top_grid to the app
        self.add_widget(self.top_grid)


        # submit button
        self.submit = Button(text="Submit", font_size=32)
        # bind the button
        self.submit.bind(on_press=self.press)
        self.add_widget(self.submit) # (will be on the left column)

    def press(self, instance):
        # assign the text input to a variable
        name = self.name.text
        pizza = self.pizza.text
        color = self.color.text

        self.add_widget(Label(text=f"Hello {name}, your favorite pizza is {pizza} and your favorite color is {color}"))
        # the text label will overflow

        # clear the input boxes
        self.name.text = ""
        self.pizza.text = ""
        self.color.text = ""



class MyApp(App):
    def build(self):
        return MyGridLayout()
    
if __name__ == "__main__":
    MyApp().run()
```