# Zone-based-density-feature-vector-extraction- (extract 26 feature)
input image size 512*512
An example of feature extraction of sinhala handwritten character

Algorithm
1st Step : Divide the original fixed size binary image in to 16 zones of 128 * 128 pixels. 
2nd Step : Computing the summation of pixels in foreground in each and every zone. And  then for obtaining each zone density, count of foreground pixels will be divided by the  total number of each zone pixels where i =1,…,16. 
3rd Step : Computing “UDRL”density (Up-Down, Right-Left), by finding the summation of  upon pixels left and right zones, and the summation of upon pixels of up and down  zones of the character image as follows: 
  upper_division= sum of on pixels in Zn1 to Zn8 zones  
  bottom_division =sum of on pixels of Zn9 to Zn16 zones  
  left_division= sum of on pixels in Zn1, Zn2, Zn5,Zn6,Zn9,Zn10,Zn13,Zn14 zones  
  right_divisiont= sum of on pixels in Zn3, Zn4,Zn7,Zn8,Zn11,Zn12,Zn15,Zn16 zones
4th Step :Computing the difference of summation on left right zone pixels the difference of  summation of up down zone pixels of the character image.  
  dv=upper_division – bottom_division  
  dh=left_division - right_division   
5th Step : Retrieving the density of 8 zones by combining the densities of the 2 consecutive  zones as 
  (d1+d2, d3+d4, d5+d6, d7+d8, d9+d10, d11+d12, d13+d14,d15+d16) and g etting 8 distinct density features of 8 zones. 
Finally the feature vector of size 26 is consisted ( dv, dh , density features of 16 zones,  8 density features of eight zones).     
