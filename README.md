# Personal-Health-Risk-Tracker
package com.edutrack.entity;

import jakarta.persistence.*;
import java.time.LocalDateTime;

@Entity
@Table(name = "students")
public class Student {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    private String name;
    private String email;
    private String department;
    private Integer semester;
    private Double cgpa;
    
    @Column(name = "created_at")
    private LocalDateTime createdAt;
    
    public Student() {
        this.createdAt = LocalDateTime.now();
    }
    
    // Constructors, getters, and setters
    public Student(String name, String email, String department, Integer semester) {
        this();
        this.name = name;
        this.email = email;
        this.department = department;
        this.semester = semester;
    }
    
    // Getters and setters...
    public Long getId() { return id; }
    public void setId(Long id) { this.id = id; }
    public String getName() { return name; }
    public void setName(String name) { this.name = name; }
    public String getEmail() { return email; }
    public void setEmail(String email) { this.email = email; }
    public String getDepartment() { return department; }
    public void setDepartment(String department) { this.department = department; }
    public Integer getSemester() { return semester; }
    public void setSemester(Integer semester) { this.semester = semester; }
    public Double getCgpa() { return cgpa; }
    public void setCgpa(Double cgpa) { this.cgpa = cgpa; }
    public LocalDateTime getCreatedAt() { return createdAt; }
}
