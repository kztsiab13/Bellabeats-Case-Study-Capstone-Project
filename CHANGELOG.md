## Change log activities
Merged "dailyActivity_merged" datasets from "4.12.16-5.12.16" and "3.12.16-4.11.16"
Shaded dailyActivity_merged datasets 3.12.16-4.11.16 in grey to idenitify duplicates
Bolded column titles
Filled column titles cells blue
Added filters to all columns
Rounded up numerical value decimal points to (0.00) for columns: TotalDistance, TrackerDistance, LoggedActivitiesDistance, VeryActiveDistance, ModeratelyActiveDistance, LightActiveDistance, and SedentaryActiveDistance
Idenitfied duplicates by ID and date, then deleted "4.12.16" datapoints from the "dailyActivity_merged 3.12.16-4.11.16" dataset
Recolored dailyActivity_merged datasets 3.12.16-4.11.16 back to white
Added column, activity_weekday with function"=TEXT(B2, "dddd")"
Added column, activity_category with function "F(D:D <= 5000, "Sedentary", IF(D:D <=7499, "Light", IF(D:D <=10000, "Moderate", "Active")))" based on TotalSteps
Added column, total_active_mins with function "=SUM(VeryActiveMinutes, FairlyActiveMinutes, LightlyActiveMinutes)"
Added column, active_percentage with function "=DIVIDE(total_active_mins,1440)"
Added column, sedentary_percentage with function "=DIVIDE(SedentaryMinutes, 1440)"
Added column, total_workout_mins with function "=SUM(VeryActiveMinutes, FairlyActiveMinutes)
Change format values in active_percentage and sedentary_percentage to percentages
Set conditional formatting in total_workout_mins column for values < 60 mins
