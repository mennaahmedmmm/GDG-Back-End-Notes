
# Normalization : 
### 1. **First Normal Form (1NF)**
   - **Goal**: Ensure each cell has only one value, and rows are unique.
   - **Example**: Suppose a table has students and their favorite fruits.

   | StudentID | Name  | Favorite_Fruit          |
   |-----------|-------|-------------------------|
   | 1         | Ahmed | Apple, Banana           |  _(Not 1NF)_

   - **In 1NF**: Split each fruit into its own row.

   | StudentID | Name  | Favorite_Fruit |
   |-----------|-------|----------------|
   | 1         | Ahmed | Apple          |
   | 1         | Ahmed | Banana         |

---

### 2. **Second Normal Form (2NF)**
   - **Goal**: Eliminate partial dependencies; each non-key column should depend on the entire primary key.
   - **Example**: Suppose a table has students, courses, and course names.

   | StudentID | CourseID | CourseName |
   |-----------|----------|------------|
   | 1         | 101      | Math       |  _(Not 2NF because `CourseName` depends only on `CourseID`, not both)_

   - **In 2NF**: Move `CourseName` to a separate `Courses` table.

   **Students_Courses Table**:

   | StudentID | CourseID |
   |-----------|----------|
   | 1         | 101      |

   **Courses Table**:

   | CourseID | CourseName |
   |----------|------------|
   | 101      | Math       |

---

### 3. **Third Normal Form (3NF)**
   - **Goal**:  **Remove transitive dependencies**, meaning no column should depend on other non-key columns.
   - **Example**: Suppose a table has `StudentID`, `ZipCode`, and `City`.

   | StudentID | ZipCode | City       |
   |-----------|---------|------------|
   | 1         | 12345   | Cairo      | _(Not 3NF because `City` depends on `ZipCode` instead of `StudentID` alone)_

   - **In 3NF**: Move `City` and `ZipCode` to a separate table.

   **Students Table**:

   | StudentID | ZipCode |
   |-----------|---------|
   | 1         | 12345   |

   **Locations Table**:

   | ZipCode | City       |
   |---------|------------|
   | 12345   | Cairo      |

---

### 4. **Fourth Normal Form (4NF)**
   - **Goal**: **Eliminate multi-valued dependencies** by separating unrelated multi-valued attributes.
   - **Example**: Suppose a student can have multiple hobbies and languages.

   | StudentID | Hobby   | LanguageKnown |
   |-----------|---------|---------------|
   | 1         | Soccer  | English       |  _(Not 4NF because `Hobby` and `LanguageKnown` are independent but repeated)_

   - **In 4NF**: Split into separate tables for hobbies and languages.

   **StudentHobbies Table**:

   | StudentID | Hobby   |
   |-----------|---------|
   | 1         | Soccer  |

   **StudentLanguages Table**:

   | StudentID | LanguageKnown |
   |-----------|---------------|
   | 1         | English       |

---

### 5. **Fifth Normal Form (5NF)**
   - **Goal**: Eliminate redundancy by breaking down tables with complex relationships.
   - **Example**: Suppose toys are categorized by character, color, and activity.

   | ToyID | Character  | Color | Activity |
   |-------|------------|-------|----------|
   | 1     | Superhero  | Blue  | Jumping  |
   | 1     | Superhero  | Blue  | Flying   | _(Not 5NF because character, color, and activity have redundancies in different combinations)_

   - **In 5NF**: Create separate tables for each attribute and link only the unique combinations.

   **ToyCharacters Table**:

   | ToyID | Character  |
   |-------|------------|
   | 1     | Superhero  |

   **ToyColors Table**:

   | ToyID | Color |
   |-------|-------|
   | 1     | Blue  |

   **ToyActivities Table**:

   | ToyID | Activity |
   |-------|----------|
   | 1     | Jumping  |
   | 1     | Flying   |
