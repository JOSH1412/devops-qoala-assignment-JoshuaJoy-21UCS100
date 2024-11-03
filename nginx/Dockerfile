# FIXED: Removed typo in 'latest' (was 'latests')
FROM nginx:latest

# FIXED: Corrected config file name typo (was 'nginix.conf')
COPY nginx.conf /etc/nginx/nginx.conf

# FIXED: Changed "eighty" to numeric 80
EXPOSE 80

# FIXED: Corrected daemon syntax 
CMD ["nginx", "-g", "daemon off;"]