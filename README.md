Sudent Management System
'''Buổi 1: Student

#1. Create a project
--
'''composer create-project laravel/laravel StudentManagement
--
#2. Start web server 
--
'''php artisan serve
http://127.0.0.1:8000/
--
#3. Create the table 
--
'''php artisan make:migration create_students_table
--
Add
            '''$table->string(‘name’);
            $table->string(‘address’);
            $table->string(‘mobile’);
--

#4. php artisan migrate
--
--
#5. Create Controller
--
php artisan make:controller StudentController --resource
--
#6. Create Model
--
'''php artisan make:model Student

add
    "protected $table = 'students';
    protected $primaryKey = 'id';
    protected $fillable = ['name', 'address', 'mobile'];"
--

#7. Create Views
--
--
#8. Routes
--

# Buổi 2: Teacher
## Tạo model Teacher và bảng teachers
---
php artisan make:model Tearcher -m

---

# Buổi 3: Courses
## Tạo model Course và bảng courses

---
php artisan make:model Course -m
---
---
-Thêm các trường dữ liệu vào bảng cources
            '''$table->id();
            $table->string('name');
            $table->string('syllabus');
            $table->string('duration'); 
            $table->timestamps()
---
---
- Sửa file Course model
   ''' protected $table = 'courses';
    protected $primaryKey = 'id';
    protected $fillable = ['name', 'syllabus', 'duration'];
---
### Tạo controller
---
php artisan make:controller CourseController --resource
---
---
- Tạo cấu trúc thư mục và các file index, create, show ... trong views giống
Teacher và Student
---





