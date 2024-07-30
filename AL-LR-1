# Input Output Class
class IO:
    def __init__(self):
        self.X = []
        self.Y = []

    def user_input(self):
        while True:
            print("Enter X Values:")
            self.X.append(float(input("Enter:\n")))
            if input("Stop? Y/N:") == 'Y':
                break
        while True:
            print("Enter Y Values:")
            self.Y.append(float(input("Enter:\n")))
            if len(self.X) == len(self.Y):
                break

    def user_output(self):
        print(self.X)
        print(self.Y)
        

# Fitting Class
class Fit(IO):
    def __init__(self):
        super().__init__()  # Initialize the parent class
        self.slope_numerator = 0
        self.slope_denominator = 0
        self.x_mean = 0
        self.y_mean = 0
        self.y_intercept = 0
        self.slope = 0  

    def Linear_regressor(self):
        self.x_mean = sum(self.X) / len(self.X)
        self.y_mean = sum(self.Y) / len(self.Y)
    
        for i in range(len(self.X)):
            self.slope_numerator += (self.X[i] - self.x_mean) * (self.Y[i] - self.y_mean)
            self.slope_denominator += (self.X[i] - self.x_mean) ** 2
        
        self.slope = self.slope_numerator / self.slope_denominator
        self.y_intercept = self.y_mean - self.slope * self.x_mean
        
# Prediction Class
class Prediction(Fit):
    def __init__(self):
        super().__init__()  # Initialize the parent class

    def predict(self):
        predict_input = float(input("Enter the number to predict:"))
        predict_output = self.slope * predict_input + self.y_intercept
        return predict_output


# Execution
OBJ = Prediction()
OBJ.user_input()
OBJ.user_output()
OBJ.Linear_regressor()
result = OBJ.predict()
print("The prediction is ", result)
