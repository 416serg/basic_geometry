import math


class Parallelogram(object):
    def __init__(self, base, side, theta):
        self.base = float(base)
        self.side = float(side)
        self.theta = float(theta)
     
    def __str__(self):
        return ("a Parallelogram with side lengths {0} and " 
                "{1}, and interior angle {2}".format(self.base, 
                                                     self.side, 
                                                     self.theta))
    
    def area(self):
        theta_angle = math.radians(self.theta)
        return (self.base * self.side * math.sin(theta_angle))
            
            
class Rectangle(Parallelogram):
    def __init__(self, base, side):
        Parallelogram.__init__(self, base, side, theta=90.0)
    
    def __str__(self):
        return "a Rectangle with side lengths {0} and {1}".format(
            self.base, self.side)  
    
    def area(self):
        return (Parallelogram.area(self))
    

class Rhombus(Parallelogram):
    def __init__(self, base, theta):
        side = base
        Parallelogram.__init__(self, base, side, theta)
        
    def __str__(self):
        return ("a Rhombus with side length {0} and interior "
                "angle {1}".format(self.base, self.theta))
    
    def area(self):
        return (Parallelogram.area(self))    
        
            
class Square(Rectangle, Rhombus):
    def __init__(self, base):
        side = base
        Rectangle.__init__(self, base, side)
    
    def __str__(self):
        return "a Square with side length {0}".format(self.base)
    
    def area(self):
        return (Rectangle.area(self))
