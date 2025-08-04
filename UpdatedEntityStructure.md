# Base

- id
- createdAt
- updatedAt
- createdBy
- updatedBy
- isDeleted
- x1
- x2

# User

- username
- password
- email
- roleName
- enabled

## RoleName

    - Enum: { ROLE_ADMIN, ROLE_USER }

# Tenant inherits Base

- User [One to One]
- Room [One to One]
- moveInDate
- contactNumber
- gender

<!-- @Entity
@Table(name = "tenants")
public class Tenant {
    @Id
    private Long id; // same as User ID

    @OneToOne
    @MapsId
    @JoinColumn(name = "id")
    private User user;

    private String address;
    private String roomNumber;
    private LocalDate moveInDate;
    // other tenant-specific fields
} -->

# Room inherits Base

- roomNo
- roomType
- floor
- size
- rentAmount
- currentOccupancy
- maxOccupancy
- isAvailable
- maintenanceCharges
- electricityCharges
- deposit
- facilities(one to many)
- tenantType
- photoUrl

## RoomType

    - Enum { single, doubleSharing, threeSharing, fourSharing }

## TenantType

    - Enum { femaleOnly, maleOnly, unisex }

# Facility inherits Base

- name
- category

## Category

    - Enum { Basic, Safety and hygiene, lifestyle and extras }

# Payment inherits Base

- tenant [Many to One - Bidirectional]
- amount
- paymentType
- paymentMethod
- timeStamp
- status (success/failure)
- additionalComment
- razorpayPaymentId
- razorpayOrderId

## PaymentType

    - Enum { rent, registrationAmount }

## PaymentMethod

    Enum { , , etc}

# LeaveNotice inherits Base

- tenant [One to One]
- moveOutDate
- reason
- settlementRemarks
- settlementStatus
- settlementReviewNotes
- settlementDeduction (Amount to be deducted from the security deposit)
- settlementProcessedDate (Date when the amount is transferred to the user)

# Complaint inherits Base

- title
- issue (description about the complaint)
- complaintStatus
- priorityLevel
- resolvedDate
- actionTaken
- tenant [Many to One]

## PriorityLevel

    - Enum { High, Low, Moderate, general, important, urgent }

## ComplaintStatus

    - Enum {Pending, Resolved, underReview}

# NoticeBoard inherits Base

- title
- message
- from
- priorityLevel

## From

    Enum {Admin, Owner, HouseKeeping}

# Responsibility Division

Tanvi -- User, Tenant
Shruti -- Room, Facility
Prajkta -- Complaint, NoticeBoard
Nivedita -- Payment, LeaveNotice
