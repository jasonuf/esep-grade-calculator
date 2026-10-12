# ESEP Grade Calculator

This library is a simple utility to calculate your grades.

Runtime requirements:
Golang 1.24+

Run unit tests (must be run from the directory /grade-calculator):
```
cd grade-calculator/
go test ./...
```

Run unit tests with code coverage:
```
cd grade-calculator/
go test -coverprofile=coverage.txt ./...
```

grade_calculator.go defines a GradeCalculator and a GradeType enum (Assignment, Exam, Essay). You create one with NewGradeCalculator() and add scores with AddGrade(name, score, type). GetFinalGrade() averages each category, weights them 50% assignments, 35% exams and 15% essays, and returns a letter grade from A to F.