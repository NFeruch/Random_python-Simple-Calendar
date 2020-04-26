daysOfWeek = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
charsOfDays = [None] * (len(daysOfWeek))
activitiesOfWeek = [None] * (len(daysOfWeek))
x = 'Your activities for the week are: '
numberDay = 0
userHasChangedCalendar = 0
assuranceOfTermination = 'yes'


def lengthOfDays():
    for L in range(0, 7):
        charsOfDays[L] = len(daysOfWeek[L])


def initialAcitivities():
    for i in range(0, 7):
        spaceNeeded = (max(charsOfDays) - charsOfDays[i] + 1)
        spaces = ' ' * spaceNeeded
        activitiesOfWeek[i] = str(input('What will the activity for ' + daysOfWeek[i] + spaces + 'be?... '))


def activitiesLister(x):
    print('-' * (len(x) - 1))
    print(x)
    for i in range(0, 7):
        print('\t' + str(daysOfWeek[i][0]) + '- ' + str(activitiesOfWeek[i]))


def changeOfCalendar(assuranceOfTermination, userHasChangedCalendar, numberDay):
    changeOfCalendar = input('Would you like to change the activity for any of the days? Please type \'yes\' if yes and \'no\' if not... ').casefold()
    if changeOfCalendar != 'yes' and changeOfCalendar != 'no':
        while changeOfCalendar != 'yes' or changeOfCalendar != 'no':
            changeOfCalendar = input('Error, please type \'yes\' if yes and \'no\' if not... ')
            if changeOfCalendar == 'yes' or changeOfCalendar == 'no':
                break
    while changeOfCalendar == 'yes':
        assuranceOfTermination = 'yes'
        userHasChangedCalendar += 1
        numberDay = int(input('''\n+ Please type the number of the day for which you would like to change the activity
  (i.e. 0 for Monday, 1 for Tuesday, up until 6 for Sunday... )'''))
        while numberDay < 0 or numberDay > 6:
            numberDay = int(input('Error, the selection is only valid for numbers 0 - 6... '))
        activitiesOfWeek[numberDay] = input('+ Please enter the activity you would like on {0} - '.format(daysOfWeek[numberDay]))
        changeOfCalendar = input('\nWould you like to change the activity for any other day?... ').casefold()
        if changeOfCalendar != 'yes' and changeOfCalendar != 'no':
            while changeOfCalendar != 'yes' or changeOfCalendar != 'no':
                changeOfCalendar = input('Error, please type \'yes\' if yes and \'no\' if not... ')
                if changeOfCalendar == 'yes' or changeOfCalendar == 'no':
                    break
        if changeOfCalendar == 'no':
            assuranceOfTermination = input('\n\t---Are you certain you don\'t want to change anything else on your calendar? ')
            if assuranceOfTermination == 'yes':
                break
            else:
                continue

    if changeOfCalendar == 'no':
        print('-' * (len(x) - 1))
        print('Your new activities for the week are: ')
        for i in range(0, 7):
            print('\t' + str(daysOfWeek[i][0]) + '- ' +str(activitiesOfWeek[i]))
        print('Have a good week!')


lengthOfDays()
initialAcitivities()
activitiesLister(x)
print('-' * (len(x) - 1))

changeOfCalendar(assuranceOfTermination, userHasChangedCalendar, numberDay)

if userHasChangedCalendar != 0:
    print('-' * (len(x) - 1))
    print('Your new activities for the week are: ')
    for i in range(0, 7):
        print('\t' + str(daysOfWeek[i][0]) + '- ' + str(activitiesOfWeek[i]))
