#include <stdio.h>

int isLeapYear(int year) {
    return (year % 4 == 0 && year % 100 != 0) || (year % 400 == 0);
}

int getDaysInMonth(int month, int year) {
    int daysInMonth[] = {0, 31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};

    if (month == 2 && isLeapYear(year)) {
        return 29;
    }

    return daysInMonth[month];
}

void printCalendar(int month, int year) {
    printf("\n===== Calendar for %d-%02d =====\n", year, month);

    // Print the header
    printf("Sun Mon Tue Wed Thu Fri Sat\n");

    // Get the day of the week for the first day of the month
    int firstDay = 1; // Assuming the first day is the 1st of the month
    int dayOfWeek = (firstDay - 1 + 7) % 7;

    // Print leading spaces
    for (int i = 0; i < dayOfWeek; i++) {
        printf("    ");
    }

    // Print the days
    for (int day = 1; day <= getDaysInMonth(month, year); day++) {
        printf("%3d ", day);

        // Move to the next line after Saturday
        if ((day + dayOfWeek) % 7 == 0) {
            printf("\n");
        }
    }

    printf("\n");
}

int main() {
    int year, month;

    // Get input from the user
    printf("Enter the year: ");
    scanf("%d", &year);

    printf("Enter the month (1-12): ");
    scanf("%d", &month);

    // Validate input
    if (year < 1 || month < 1 || month > 12) {
        printf("Invalid input. Please enter a valid year and month.\n");
        return 1;
    }

    // Display the calendar
    printCalendar(month, year);

    return 0;
}
