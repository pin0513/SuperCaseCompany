---
name: Shift Scheduling
description: Design and implement shift scheduling systems for restaurants, breakfast shops, beverage shops, and other service businesses
---

# Shift Scheduling Skill

## Purpose

Provide comprehensive shift scheduling system design and implementation guidance for service-based businesses, addressing labor law compliance, skill-based matching, peak demand handling, and employee preferences.

## When to Use This Skill

Use this skill when:
- Client needs employee shift scheduling system
- Requirements include labor law compliance
- Business has peak and off-peak periods
- Staff have varying skills and certifications
- Multi-location scheduling coordination needed
- Manager approval workflows required

## Core Components

### 1. Shift Template Management

Design shift templates for recurring schedules:
- Define shift types (opening, rush, closing, on-call)
- Set shift time windows (start, end, break periods)
- Specify required staff count and skill mix
- Configure wage rates and overtime rules
- Set location and department assignments

**Example Template**:
```
Shift: Morning Rush (Restaurant)
Time: 11:00 AM - 3:00 PM
Required Staff:
  - Kitchen: 5 (2 certified cooks, 3 prep staff)
  - Front-of-House: 8 (1 host, 6 servers, 1 cashier)
  - Management: 1 (shift supervisor)
Labor Budget: 14 staff-hours x average wage
```

### 2. Labor Law Compliance

Ensure scheduling complies with regulations:
- Maximum consecutive hours (8-hour shifts, overtime approval)
- Mandatory break periods (30-min lunch, 15-min breaks)
- Minor restrictions (no work past 10pm, max 8 hours/day)
- Overtime thresholds and rates (1.5x after 40 hours/week)
- Rest period requirements (10 hours between shifts)

**Compliance Checks**:
- Alert when staff scheduled >8 hours without overtime approval
- Block scheduling minors outside permitted hours
- Enforce break periods based on shift length
- Warn when rest period between shifts <10 hours
- Calculate overtime automatically when thresholds exceeded

### 3. Skill-Based Matching

Match staff skills to shift requirements:
- Define skill categories (certifications, experience levels)
- Set skill requirements per shift or position
- Priority-rank staff by skill level and seniority
- Ensure minimum certified staff per shift
- Support cross-training and skill development tracking

**Example Matching**:
```
Shift Requirement: Certified Food Handler
Available Staff:
  - Alice: Certified, 3 years experience (Priority 1)
  - Bob: Certified, 1 year experience (Priority 2)
  - Carol: Not certified, 6 months experience (Cannot assign)

System assigns Alice or Bob, alerts if neither available
```

### 4. Availability and Preferences

Incorporate employee availability and preferences:
- Collect staff availability (days/times available to work)
- Capture preferences (preferred shifts, days off requests)
- Handle time-off requests and approvals
- Support shift swap requests between employees
- Balance fairness (distribute desirable shifts equitably)

**Workflow**:
1. Employee submits availability and preferences
2. Manager reviews and approves/denies requests
3. Scheduling algorithm considers approved availability
4. System maximizes preference matches while meeting coverage
5. Employees receive draft schedule for feedback

### 5. Demand Forecasting

Forecast staffing needs based on demand:
- Historical sales data analysis (peak hours, days, seasons)
- Special events and holidays consideration
- Weather and external factors impact
- Staffing ratios (sales per labor hour targets)
- Dynamic adjustments based on real-time data

**Forecasting Model**:
```
Input: Historical sales data (past 12 weeks)
Analysis: Identify patterns (weekday vs. weekend, lunch vs. dinner)
Forecast: Predict next week's hourly sales
Staffing: Calculate required staff based on sales/labor ratio
Output: Recommended shift coverage by hour/day
```

### 6. Multi-Location Coordination

Coordinate scheduling across multiple locations:
- Centralized staff pool (share staff across locations)
- Location-specific shift templates
- Cross-location coverage requests
- Manager visibility across assigned locations
- Consolidated labor cost reporting

**Use Case**:
```
Chain with 10 locations:
  - Each location has dedicated core staff
  - Floating staff can cover multiple locations
  - Manager sees all assigned location schedules
  - Cross-location coverage for unexpected absences
  - Corporate dashboard shows labor cost across all locations
```

### 7. Approval Workflows

Implement approval processes for scheduling:
- Draft schedule creation and review
- Manager approval before publishing
- Overtime approval for >8 hour shifts
- Time-off request approvals
- Shift swap approval by manager

**Approval Hierarchy**:
```
1. Shift Supervisor: Approve daily shift changes
2. Store Manager: Approve weekly schedules and time-off
3. Regional Manager: Approve overtime budget overruns
4. HR: Approve labor law exceptions (rare)
```

### 8. Real-Time Adjustments

Handle dynamic scheduling changes:
- Call-in/no-show staff replacement
- On-call staff notification and confirmation
- Shift extensions for unexpected busy periods
- Early release when business is slow
- Emergency coverage requests

**Emergency Coverage Workflow**:
```
Scenario: Server calls in sick 2 hours before shift
1. System identifies available on-call staff
2. Sends notification to on-call staff (SMS, app)
3. First responder confirms availability
4. Manager approves replacement
5. Schedule updated and published
6. Payroll records emergency call-in premium
```

## Implementation Checklist

### Requirements Phase
- [ ] Identify business type and operating hours
- [ ] Document shift patterns (rush hours, coverage needs)
- [ ] Collect labor law requirements by jurisdiction
- [ ] Define staff skill categories and certifications
- [ ] Determine approval hierarchy and workflows
- [ ] Assess multi-location coordination needs

### Design Phase
- [ ] Design shift template structure
- [ ] Define labor law compliance rules
- [ ] Model skill-based matching algorithm
- [ ] Design employee availability/preference interface
- [ ] Plan demand forecasting approach
- [ ] Design manager approval workflows

### Development Phase
- [ ] Build shift template management
- [ ] Implement labor law compliance checks
- [ ] Develop skill-based assignment logic
- [ ] Create employee self-service portal
- [ ] Integrate demand forecasting
- [ ] Implement approval workflows
- [ ] Build real-time adjustment features

### Testing Phase
- [ ] Test all labor law compliance scenarios
- [ ] Validate skill-based matching logic
- [ ] Test multi-location coordination
- [ ] Verify approval workflows
- [ ] Load test for large staff counts (>100 employees)
- [ ] User acceptance testing with managers and staff

## Success Metrics

Measure scheduling system effectiveness:
- **Labor Cost %**: Target 25-35% of revenue (varies by industry)
- **Schedule Compliance**: >95% of shifts filled
- **Employee Satisfaction**: >75% satisfied with schedule
- **Manager Time Savings**: 50% reduction in manual scheduling time
- **Labor Law Violations**: 0 post-deployment
- **Overtime Control**: <5% of total labor hours

## Common Challenges and Solutions

| Challenge | Solution |
|-----------|----------|
| Staff request same desirable shifts | Rotate desirable shifts fairly, priority by seniority |
| Last-minute call-ins and no-shows | On-call staff pool, automated notification system |
| Complex labor laws (multiple jurisdictions) | Configurable rule engine, regular compliance audits |
| Demand forecasting inaccuracy | Machine learning on historical data, manager overrides |
| Employee resistance to digital scheduling | Mobile app, easy shift swaps, transparent fairness |
| Multi-location staff sharing complexity | Clear home location assignment, travel time compensation |

## Integration Requirements

Shift scheduling integrates with:
- **POS System**: Sales data for demand forecasting
- **Payroll System**: Hours worked, overtime, pay rates
- **HR System**: Employee data, certifications, employment status
- **Time Clock**: Actual clock-in/out vs. scheduled
- **Communication**: SMS, push notifications for schedule changes

## Industry-Specific Considerations

### Restaurants
- Front-of-house (servers, hosts) vs. back-of-house (kitchen) split
- Table section assignments within shift
- Tipping and tip pool coordination
- Health permit and food handler certification tracking

### Breakfast Shops
- Early morning shifts (4am-6am) with premium pay
- High concentration of shifts in 6am-11am window
- Limited evening hours or closed by 2pm
- Equipment opening and closing procedures

### Beverage Shops
- Barista skill levels (trainee, certified, master)
- Equipment cleaning and maintenance tasks
- Peak hours (morning coffee rush, afternoon tea rush)
- Seasonal staffing adjustments (summer higher demand)

### Cold Chain Logistics
- 24/7 operations and shift rotations
- Forklift and equipment certifications
- Temperature monitoring responsibilities
- Shift handoff procedures for inventory status

## Example Input/Output

### Input: Weekly Schedule Request
```
Business: Coffee shop with 2 locations
Week: March 1-7, 2026
Operating Hours: 7am-8pm daily
Staff Pool: 12 baristas (6 per location)
Special Events: March 5 (Saturday) local festival (expect +50% traffic)

Constraints:
- Each shift needs 1 certified barista minimum
- No staff work >5 consecutive days
- Alice requested March 3-4 off (approved)
- Bob available only evenings (student)
```

### Output: Generated Schedule
```
Location 1: Main Street
March 1 (Mon):
  - Morning (7am-1pm): Alice (certified), Carol
  - Afternoon (1pm-8pm): Dave (certified), Bob

March 2 (Tue):
  - Morning (7am-1pm): Carol, Eve
  - Afternoon (1pm-8pm): Alice (certified), Bob

March 3 (Wed):
  - Morning (7am-1pm): Dave (certified), Eve
  - Afternoon (1pm-8pm): Carol, Bob
  (Note: Alice off - requested)

March 5 (Sat) - Festival Day:
  - Morning (7am-1pm): Alice (certified), Carol, Eve (3 staff - high demand)
  - Afternoon (1pm-8pm): Dave (certified), Bob, Frank (3 staff - high demand)

Alerts:
  - March 5: Additional staff scheduled due to forecasted +50% demand
  - All shifts have minimum 1 certified barista
  - No labor law violations detected
```

## References

- U.S. Department of Labor: Fair Labor Standards Act (FLSA)
- Taiwan Labor Standards Act (勞動基準法)
- Industry-specific labor law resources
- Workforce scheduling best practices (SHRM, Workforce Institute)

## Version History

- v1.0 (2026-02-11): Initial skill creation for Dimension 7 Industry Experts
