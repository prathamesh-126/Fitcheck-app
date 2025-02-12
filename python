class FitCheck:
    def _init_(self):
        # Ideal weight and height ranges for different age groups and genders
        self.ideal_data = {
            15: {
                "male": {"weight": (45, 55), "height": (162, 168)},
                "female": {"weight": (45, 52), "height": (158, 163)}
            },
            16: {
                "male": {"weight": (47, 60), "height": (165, 173)},
                "female": {"weight": (46, 53), "height": (159, 164)}
            },
            17: {
                "male": {"weight": (48, 62), "height": (168, 175)},
                "female": {"weight": (48, 56), "height": (160, 165)}
            },
            18: {
                "male": {"weight": (50, 65), "height": (170, 175)},
                "female": {"weight": (50, 60), "height": (161, 166)}
            },
            19: {
                "male": {"weight": (53, 68), "height": (171, 180)},
                "female": {"weight": (53, 65), "height": (162, 167)}
            },
            20: {
                "male": {"weight": (56, 73), "height": (160, 180)},
                "female": {"weight": (55, 69), "height": (160, 175)}
            },
            "21-25": {
                "male": {"weight": (50, 65), "height": (170, 185)},
                "female": {"weight": (50, 62), "height": (158, 172)}
            },
            "26-30": {
                "male": {"weight": (53, 70), "height": (168, 183)},
                "female": {"weight": (53, 67), "height": (157, 171)}
            },
            "31-35": {
                "male": {"weight": (59, 73), "height": (166, 181)},
                "female": {"weight": (59, 70), "height": (156, 170)}
            },
            "36-40": {
                "male": {"weight": (61, 76), "height": (165, 180)},
                "female": {"weight": (60, 74), "height": (155, 169)}
            },
            "41-45": {
                "male": {"weight": (62, 77), "height": (163, 178)},
                "female": {"weight": (60, 76), "height": (153, 167)}
            },
            "46-50": {
                "male": {"weight": (63, 80), "height": (160, 175)},
                "female": {"weight": (62, 78), "height": (150, 165)}
            }
        }

    def get_user_input(self):
        self.age = int(input("Enter your age: "))
        """if self.age<15:
            continue
            #print("Please enter age above 15.")"""
        self.gender = input("Enter your gender (male/female): ").strip().lower()
        self.weight = float(input("Enter your current weight (kg): "))
        self.height = float(input("Enter your current height (cm): "))
        print("\nHealth Analysis:")

    def get_age_group(self):
        if 21 <= self.age <= 25:
            return "21-25"
        elif 26 <= self.age <= 30:
            return "26-30"
        elif 31 <= self.age <= 35:
            return "31-35"
        elif 36 <= self.age <= 40:
            return "36-40"
        elif 41 <= self.age <= 45:
            return "41-45"
        elif 46 <= self.age <= 50:
            return "46-50"
        else:
            return None
        
    def analyze_data(self):
        age_group = self.get_age_group()
        if self.age in self.ideal_data and self.gender in self.ideal_data[self.age]:
            ideal_weight_range = self.ideal_data[self.age][self.gender]["weight"]
            ideal_height_range = self.ideal_data[self.age][self.gender]["height"]

            weight_diff = 0
            height_diff = 0

            if self.weight < ideal_weight_range[0]:
                weight_diff = self.weight - ideal_weight_range[0]
                print(f"Weight difference: {weight_diff} kg")
                print("You are underweight.\n")
            elif self.weight > ideal_weight_range[1]:
                weight_diff = self.weight - ideal_weight_range[1]
                print(f"Weight difference: {weight_diff} kg")
                print("You are overweight.")

            if self.height < ideal_height_range[0]:
                height_diff = self.height - ideal_height_range[0]
                print(f"Height difference: {height_diff} cm")
                print("Your height is short as per our data.\n")
            elif self.height > ideal_height_range[1]:
                height_diff = self.height - ideal_height_range[1]
                print(f"Height difference: {height_diff} cm")
                print("Your height is perfect.\n")

            return weight_diff, height_diff
        
        elif age_group and self.gender in self.ideal_data[age_group]:
            ideal_weight_range = self.ideal_data[age_group][self.gender]["weight"]
            ideal_height_range = self.ideal_data[age_group][self.gender]["height"]

            weight_diff = 0
            height_diff = 0

            if self.weight < ideal_weight_range[0]:
                weight_diff = self.weight - ideal_weight_range[0]
                print(f"Weight difference: {weight_diff} kg")
                print("You are underweight.\n")
            elif self.weight > ideal_weight_range[1]:
                weight_diff = self.weight - ideal_weight_range[1]
                print(f"Weight difference: {weight_diff} kg")
                print("You are overweight.")

            if self.height < ideal_height_range[0]:
                height_diff = self.height - ideal_height_range[0]
                print(f"Height difference: {height_diff} cm")
                print("Your height is short as per our data.\n")
            elif self.height > ideal_height_range[1]:
                height_diff = self.height - ideal_height_range[1]
                print(f"Height difference: {height_diff} cm")
                print("Your height is perfect.\n")

            return weight_diff, height_diff
        else:
            return None, None

    def display_recommendations(self, weight_diff, height_diff):
        """print("\nHealth Analysis:")
        print(f"Weight difference: {weight_diff} kg")
        print(f"Height difference: {height_diff} cm")"""

        if weight_diff < 0:
            if self.gender=='male':
                if 15<= self.age <=25:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight gain.")
                    print("Breakfast (8:00-8:30AM) : 2 egg brown bread sandwich + green chutney + 1 cup milk + 3 cashews + 4 almonds + 2 walnuts.")
                    print("Mid-Meal (11:00-11:30AM): 1 cup banana shake.")
                    print("Lunch (2:00-2:30PM) : 1 cup arhar dal + 1 cup potato curry + 3 chapatti + 1/2 cup rice + 1/2 cup low fat curd + salad.")
                    print("Evening (4:00-4:30PM) : 1 cup strawberry smoothie + 1 cup vegetable poha.")
                    print("Dinner (8:00-8:30PM) : 1.5 cup chicken curry + 3 chapati + salad.")

                elif 26<= self.age <=35:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight gain.")
                    print("Breakfast (8:00-8:30AM) : 3 onion stuffed paratha + 1 cup curd + 3 cashews + 4 almonds + 2 walnuts")
                    print("Mid-Meal (11:00-11:30AM) : 1 cup mango shake.")
                    print("Lunch (2:00-2:30PM) : 1 cup moong dal/ chicken curry + 1 cup potato and cauliflower vegetable + 3 chapatti + 1/2 cup rice + salad.")
                    print("Evening (4:00-4:30PM) : 1 cup pomegranate juice + 2 butter toasted bread.")
                    print("Dinner (8:00-8:30PM)	1 cup beans potato vegetable + 3 chapatti + salad.")

                elif 36<= self.age <=50:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight gain.")
                    print("Breakfast (8:00-8:30AM) : 2 cup vegetable poha + 1 cup curd + 3 cashews + 4 almonds + 2 walnuts.")
                    print("Mid-Meal (11:00-11:30AM) : 2 cups watermelon juice.")
                    print("Lunch (2:00-2:30PM) : 1 cup chana dal + 1 cup bhindi vegetable + 3 chapatti + 1/2 cup rice + salad.")
                    print("Evening (4:00-4:30PM) : 1 cup sprouts salad + 2 potato cheela + green chutney.")
                    print("Dinner (8:00-8:30PM)	1 cup peas mushroom vegetable + 3 chapatti + salad.")

            elif self.gender=="female":
                if 15<= self.age <=25:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight gain")
                    print("Breakfast (8:00-8:30AM) : 1 serving Raspberry-Peach-Mango Smoothie Bowl + 1 hard-boiled egg.")
                    print("Mid-Meal (11:00-11:30AM) : 15 baby carrots + 3 Tbsp. hummus + 1 medium orange.")
                    print("Lunch (2:00-2:30PM) : 1 serving Roasted Butternut Squash & Root Vegetables with Cauliflower Gnocchi + 1 slice whole-wheat toast with 1 tsp. unsalted butter.")
                    print("Evening (4:00-4:30PM) : 1 serving Homemade Microwave Popcorn + 1 large banana + 8 unsalted almonds.")
                    print("Dinner (8:00-8:30PM) : 2 servings Philly Cheese Steak Sloppy Joes + 2 cups fresh spinach, 1 cup shredded carrots topped with 1/2 Tbsp. olive oil and 1/2 Tbsp. balsamic vinegar.")

                elif 26<= self.age <=35:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight gain")
                    print("Breakfast (8:00-8:30AM) : 1 serving Raspberry-Peach-Mango Smoothie Bowl + 1 hard-boiled egg.")
                    print("Mid-Meal (11:00-11:30AM) : 15 baby carrots + 3 Tbsp. hummus + 1 medium orange.")
                    print("Lunch (2:00-2:30PM) : 1 serving Roasted Butternut Squash & Root Vegetables with Cauliflower Gnocchi + 1 slice whole-wheat toast with 1 tsp. unsalted butter.")
                    print("Evening (4:00-4:30PM) : 1 serving Homemade Microwave Popcorn + 1 large banana + 8 unsalted almonds.")
                    print("Dinner (8:00-8:30PM) : 2 servings Philly Cheese Steak Sloppy Joes + 2 cups fresh spinach, 1 cup shredded carrots topped with 1/2 Tbsp. olive oil and 1/2 Tbsp. balsamic vinegar.")

                elif 36<= self.age <=50:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight gain")
                    print("Breakfast (8:00-8:30AM) : 2 servings Maple-Nut Granola + 1 cup 2% milk.")
                    print("Mid-Meal (11:00-11:30AM) : 15 carrot sticks + 1/4 cup hummus + 1 medium orange.")
                    print("Lunch (2:00-2:30PM) : 1 serving Roasted Butternut Squash & Root Vegetables with Cauliflower Gnocchi + 1 slice whole-wheat toast with 1 tsp. unsalted butter.")
                    print("Evening (4:00-4:30PM) : 4 graham crackers + 1 medium apple.")
                    print("Dinner (8:00-8:30PM) : 1 serving Southern-Style Oven-Fried Chicken + 1 serving Greek Potato Salad + 1 serving Garlicky Green Beans.")
                    
            """print("\nTo increase weight:")
            print("- Eat more high-protein foods (chicken, eggs, dairy)")
            print("- Include nuts, seeds, and healthy fats")
            print("- Strength training exercises")"""

        elif weight_diff > 0:
            if self.gender=="male":
                if 15<= self.age <=25:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight loss")
                    print("Breakfast (8:00-8:30AM) : green smoothie (made with ½ banana + ½ cup frozen mango + 1 cup kale + ½ cup plain, low-fat Greek yogurt + ½ small avocado + ½ cup nonfat milk).")
                    print("Mid-Meal (11:00-11:30AM) : 1 apple + 1 oz nuts.")
                    print("Lunch (2:00-2:30PM) : 2 cups Veggie Soup.")
                    print("Evening (4:00-4:30PM) : 1 cup baby carrots & sugar snap peas + 2 tablespoons hummus.")
                    print("Dinner (8:00-8:30PM) : 4 oz salmon + 1 cup steamed carrots + 1 cup steamed broccoli + 2 tablespoons teriyaki sauce + 1 teaspoon sesame seeds.")

                elif 26<= self.age <=35:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight loss")
                    print("Breakfast (8:00-8:30AM) : berry smoothie (made with ½ banana + 1 cup frozen strawberries + ½ cup plain, low-fat Greek yogurt + ½ cup nonfat milk).")
                    print("Mid-Meal (11:00-11:30AM) : 1 banana + 1 oz nuts.")
                    print("Lunch (2:00-2:30PM) : 2 cups Veggie Soup.")
                    print("Evening (4:00-4:30PM) : 1 cup broccoli & cauliflower + 2 tablespoons tzatziki.")
                    print("Dinner (8:00-8:30PM) : 4 oz grilled chicken + ½ cup roasted sweet potatoes + 1 cup roasted Brussels sprouts + 1 tablespoon olive oil.")

                elif 36<= self.age <=50:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight loss")
                    print("Breakfast (8:00-8:30AM) : green smoothie (made with ½ banana + ½ cup frozen mango + 1 cup kale + ½ cup plain, low-fat Greek yogurt + ½ small avocado + ½ cup nonfat milk).")
                    print("Mid-Meal (11:00-11:30AM) : 1 cup blueberries + 1 oz nuts.")
                    print("Lunch (2:00-2:30PM) : 3 oz grilled chicken + ½ cup cooked quinoa + 1 cup cherry tomatoes & chopped cucumber + 2 tablespoons feta cheese + 1 tablespoon vinaigrette.")
                    print(" Evening (4:00-4:30PM) : 1 cup baby carrots & sugar snap peas + 2 tablespoons hummus.")
                    print("Dinner (8:00-8:30PM) : 4 oz mahi-mahi + 1 cup steamed carrots + 1 cup steamed broccoli + 2 tablespoons teriyaki sauce + 1 teaspoon sesame seeds.")

            elif self.gender=="female":
                if 15<= self.age <=25:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight loss")
                    print("Breakfast (8:00-8:30AM) : Overnight Oats with blueberries (made with ½ cup oats + 1 tablespoon chia seeds + ½ cup nonfat milk + ½ cup plain, low-fat Greek yogurt + ½ cup blueberries).")
                    print("Mid-Meal (11:00-11:30AM) : 1 banana + 1 oz nuts.")
                    print("Lunch (2:00-2:30PM) : 3 oz tuna + 2 cups mixed greens + 1 cup cherry tomatoes & chopped cucumber + 1 tablespoon vinaigrette.")
                    print("Evening (4:00-4:30PM) : 1 cup broccoli & cauliflower + 2 tablespoons tzatziki.")
                    print("Dinner (8:00-8:30PM) : 4 oz grilled chicken + ½ cup roasted sweet potatoes + 1 cup roasted Brussels sprouts + 1 tablespoon olive oil.")

                elif 26<= self.age <=35:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight loss")
                    print("Breakfast (8:00-8:30AM) : Overnight Oats with blueberries (made with ½ cup oats + 1 tablespoon chia seeds + ½ cup nonfat milk + ½ cup plain, low-fat Greek yogurt + ½ cup blueberries).")
                    print("Mid-Meal (11:00-11:30AM) : 1 apple + 1 oz nuts.")
                    print("Lunch (2:00-2:30PM) : 3 oz lean deli turkey + ¼ avocado + 1 whole-wheat tortilla + 1 cup mixed greens.")
                    print("Evening (4:00-4:30PM) : 1 cup baby carrots & sugar snap peas + 2 tablespoons hummus.")
                    print("Dinner (8:00-8:30PM) : 4 oz shrimp + 1 cup steamed carrots + 1 cup steamed broccoli + ½ cup cooked brown rice + 2 tablespoons teriyaki sauce + 1 teaspoon sesame seeds.")

                elif 36<= self.age <=50:
                    print("So here's a planned routine for your FitCheck from today!!!")
                    print("#StayHealthy\n")
                    print("Diet for weight loss")
                    print("Breakfast (8:00-8:30AM) : 2 slices whole-wheat toast + 2 hard-boiled eggs + hot sauce (optional).")
                    print("Mid-Meal (11:00-11:30AM) : 1 cup blueberries + 1 oz nuts.")
                    print("Lunch (2:00-2:30PM) : 3 oz smoked salmon + ¼ avocado + 1 whole-wheat tortilla + 1 cup mixed greens.")
                    print("Evening (4:00-4:30PM) : 1 cup broccoli & cauliflower + 2 tablespoons tzatziki.")
                    print("Dinner (8:00-8:30PM) : 4 oz lean steak + 1 cup roasted sweet potatoes + 1 cup roasted Brussels sprouts + 1 tablespoon olive oil.")
                    
            """print("\nTo decrease weight:")
            print("- Eat more vegetables and whole grains")
            print("- Avoid junk food and sugary drinks")
            print("- Increase physical activity (cardio, HIIT)")"""

        if height_diff < 0:
            if 15<= self.age <=20:
                print("\nTo increase height:")
                print("- Running, cycling, swimming")
                print("- Stretching exercises and yoga")
                print("- Proper sleep and balanced nutrition")

    def run(self):
        self.get_user_input()
        weight_diff, height_diff = self.analyze_data()
        if weight_diff is not None:
            self.display_recommendations(weight_diff, height_diff)
        else:
            print("No data available for this age group or gender.")


# Run the app
app = FitCheck()
app.run()
