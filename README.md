# Adventure Works Dashboard

### Dashboard Link : https://drive.google.com/file/d/1SBgKtLOyg7vtWEfnevNnqZUoyyrUAe4T/view?usp=drive_link


## Problem Statement

This dashboard helps the Adventure Works understand their sales and customers better. It helps them to understand their overall/monthly revenue, top customers and details about their products. Through different KPIs and visuals, they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know which product or which customer are giving us more/less sales and hence improving ny identifying the problem.



### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in some of the columns there were some errors.
- Step 5 : In the report view, under the view tab, theme was selected.
- Step 6 : Since we have many pages in the report, one page was created for the Overview of the store, the other was for Country wise sales details, then Product details, Customer details and some AI insights were added for further reference.
- Step 7 : Many DAX measures were created for the visuals to be dynamic and also to get some deeper insights into the data.
- Step 8 : Visual filters (Slicers) were added for the user to filter the visuals according to their choice.

  

Some of the DAX expressions and their visuals are represented below:

1. Total Revenue
       
        Total Revenue = 
        SUMX(
        'Sales Data',
        'Sales Data'[OrderQuantity] * 
        RELATED(
                'Product Lookup'[ProductPrice]
        )
        )

![Total Revenue](https://private-user-images.githubusercontent.com/219225965/462514495-52e630d3-a271-498c-9a46-3bc6fb1189be.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE2MzY2NTcsIm5iZiI6MTc1MTYzNjM1NywicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNTE0NDk1LTUyZTYzMGQzLWEyNzEtNDk4Yy05YTQ2LTNiYzZmYjExODliZS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA0JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNFQxMzM5MTdaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02NjdlOTRiZGYyNjgwOTZhNWE5NzZhNWI2Y2JmNTY4MTA3MWI5NTlhMTg3M2VhZjM4MzNhNGU5ZmJhZWFkZDczJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.GKRFTb5-gN5jFhtwUslefkJZggaYtqBCSThhxKPopJ4)
        
2. Return Rate

        Return Rate = 
        DIVIDE(
        [Quantity Returned],[Quantity Sold],"No Sales"
        )

![Return_Rate](https://private-user-images.githubusercontent.com/219225965/462516043-fa578e3f-3b20-4a32-a515-406a82411ad3.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE2MzY4NDMsIm5iZiI6MTc1MTYzNjU0MywicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNTE2MDQzLWZhNTc4ZTNmLTNiMjAtNGEzMi1hNTE1LTQwNmE4MjQxMWFkMy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA0JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNFQxMzQyMjNaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02OTM2NzhkYjI5MmY3OGM3NjkyOTk4YzI4ZGYzNzYwODkxNTMxZTY0Zjg0YTczMmVhZDJkYjMxMjZjOTU1OTNhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.bcy4BLWeqAxSOsvS2EWuviIni17t4VTmtdEQl7gkFZo)

        
3. Total Orders
 
        Total Orders = 
        DISTINCTCOUNT(
        'Sales Data'[OrderNumber]
        )
 
 
 ![Snap_3](https://private-user-images.githubusercontent.com/219225965/462515423-e8f62a31-7ade-4e76-b8e0-66edb2fdcc87.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE2MzY3MzksIm5iZiI6MTc1MTYzNjQzOSwicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNTE1NDIzLWU4ZjYyYTMxLTdhZGUtNGU3Ni1iOGUwLTY2ZWRiMmZkY2M4Ny5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA0JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNFQxMzQwMzlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04MWVmOTY0MzBlZGIzYzNhZDFjYWQ2YTNiMzlmMTM0M2I2MDU3MzVlNDI5ZTc2OGQ5MGU0NDQxOTRjYmU3ZTI5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.La0_nbzr0boVQbUzal607PpXR5FQ8L7T8HK15FItuFI)

 
4. Total Returns (with Previous Month Returns)

 
         Total Returns = 
        COUNT(
    'Returns Data'[ReturnQuantity]
)
 
 ![Snap_4](https://private-user-images.githubusercontent.com/219225965/462516316-bbf9a357-289c-43ee-99c8-9d1d58e63693.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE2MzY4ODAsIm5iZiI6MTc1MTYzNjU4MCwicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNTE2MzE2LWJiZjlhMzU3LTI4OWMtNDNlZS05OWM4LTlkMWQ1OGU2MzY5My5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA0JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNFQxMzQzMDBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0wNzU5NGIwM2U2OGViYzc2NzM1NjhlOGEzNTg4MWM1MzMzOGQ4ZDAwNDI3MzRhNTQ1NDI4ZTlkMDkxZjc1OTVkJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.gF_doFoKnqiqBhA--6MHJH-3F3gmA3rYkJaQsR64maA)
 
 # Report Snapshot (Power BI DESKTOP) (Exec Dashboard)

 
![Dashboard_upload](https://private-user-images.githubusercontent.com/219225965/462517118-e00b09a5-ce31-4f47-8f6d-57abdf1e0990.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTE2MzY5OTIsIm5iZiI6MTc1MTYzNjY5MiwicGF0aCI6Ii8yMTkyMjU5NjUvNDYyNTE3MTE4LWUwMGIwOWE1LWNlMzEtNGY0Ny04ZjZkLTU3YWJkZjFlMDk5MC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzA0JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcwNFQxMzQ0NTJaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05MThmNDQ5YzZhNDNmZDhhM2QyYWExYjg0ZTk0ZGRiM2U2MDAyZGEyYWZjYjNhMmNlN2U4OWM0YTM3ZmYyMDIyJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.JQx7N0pjSP76TGhPrniQ7WRxGtBRHbVX_nKQnTnjY74)

# Insights

A seven page report was created to understand better insights of the store.

Following inferences can be drawn from the dashboard;

### [1] Exec Dashboard

   Total Revenue: $24.9 M       
   Total Profit:  $10.5 M       
   Return Rate:   2.2 %         
   Total Orders:  25.2 K        
   Monthly Revenue: $1.83 M     


           
### [2] Product Detail

        Monthly Target: 213/234
        Monthly Revenue: $1,668/$1,804
        Monthly Profit: $1,044/$1,129
  
   
  
  ### [3] Customer Detail 
  
      Unique Customers: 17.4 K
      Revenue per Customer: $1,431

 
