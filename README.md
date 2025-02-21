# LuckData-Walmart-API
LuckData Walmart API enables developers to access Walmart's extensive catalog of products, allowing integration of product search, details, and reviews directly into applications.

# How to Use

Step 1: Click “Get Started”

Step 2: Purchase a plan and complete the payment

Step 3: Choose your preferred run mode

Step 4: Click "Test Endpoint"

# Code Snippets

## python

  <pre>import requests

  headers = {
      'X-Luckdata-Api-Key': 'your api key'
  }
  
  json_data={}
  
  response = requests.get(
      'https://luckdata.io/api/walmart-API/get_vwzq?url=https://www.walmart.com/ip/NELEUS-Mens-Dry-Fit-Mesh-Athletic-Shirts-3-Pack-Black-Gray-Olive-Green-US-Size-M/439625664?classType=VARIANT',
      headers=headers,
      
  )
  print(response.json())
  </pre>

## java

  <pre>import java.io.IOException;
  import java.net.URI;
  import java.net.http.HttpClient;
  import java.net.http.HttpRequest;
  import java.net.http.HttpResponse;
  
  HttpClient client = HttpClient.newHttpClient();
  
  HttpRequest request = HttpRequest.newBuilder()
      .uri(URI.create("https://luckdata.io/api/walmart-API/get_vwzq?url=https://www.walmart.com/ip/NELEUS-Mens-Dry-Fit-Mesh-Athletic-Shirts-3-Pack-Black-Gray-Olive-Green-US-Size-M/439625664?classType=VARIANT"))
      .GET()
      
      .setHeader("X-Luckdata-Api-Key", "your api key")
      .build();
  
  HttpResponse<String> response = client.send(request, HttpResponse.BodyHandlers.ofString());</pre>

## go

    <pre>package main
  
    import (
      "fmt"
      "io"
      "log"
      "net/http"
      "strings"
    )
    
    func main() {
      client := &http.Client{}
      var data = nil
      req, err := http.NewRequest("GET", "https://luckdata.io/api/walmart-API/get_vwzq?url=https://www.walmart.com/ip/NELEUS-Mens-Dry-Fit-Mesh-Athletic-Shirts-3-Pack-Black-Gray-Olive-Green-US-Size-M/439625664?classType=VARIANT", data)
      if err != nil {
        log.Fatal(err)
      }
      
      req.Header.Set("X-Luckdata-Api-Key", "your api key")
      resp, err := client.Do(req)
      if err != nil {
        log.Fatal(err)
      }
      defer resp.Body.Close()
      bodyText, err := io.ReadAll(resp.Body)
      if err != nil {
        log.Fatal(err)
      }
      fmt.Printf("%s\n", bodyText)
    }</pre>

## shell

    <pre>curl -X GET "https://luckdata.io/api/walmart-API/get_vwzq?url=https://www.walmart.com/ip/NELEUS-Mens-Dry-Fit-Mesh-Athletic-Shirts-3-Pack-Black-Gray-Olive-Green-US-Size-M/439625664?classType=VARIANT"  -H "X-Luckdata-Api-Key":"your api key" </pre>

## C#

    <pre>using System.Net.Http;
    using System.Net.Http.Headers;
    
    HttpClient client = new HttpClient();
    
    HttpRequestMessage request = new HttpRequestMessage(HttpMethod.get, "https://luckdata.io/api/walmart-API/get_vwzq?url=https://www.walmart.com/ip/NELEUS-Mens-Dry-Fit-Mesh-Athletic-Shirts-3-Pack-Black-Gray-Olive-Green-US-Size-M/439625664?classType=VARIANT");
    
    
    request.Headers.Add("X-Luckdata-Api-Key", "your api key");
    
    request.Content = new StringContent("");
    request.Content.Headers.ContentType = new MediaTypeHeaderValue("application/json");
    
    HttpResponseMessage response = await client.SendAsync(request);
    response.EnsureSuccessStatusCode();
    string responseBody = await response.Content.ReadAsStringAsync();</pre>

## JavaScript

    <pre>fetch('https://luckdata.io/api/walmart-API/get_vwzq?url=https://www.walmart.com/ip/NELEUS-Mens-Dry-Fit-Mesh-Athletic-Shirts-3-Pack-Black-Gray-Olive-Green-US-Size-M/439625664?classType=VARIANT', {
    method: 'GET',
    headers: {
        'X-Luckdata-Api-Key': 'your api key'
    }
    })</pre>

more about : <a href="https://luckdata.io/marketplace/detail/walmart-API">LuckData-Walmart-API</a>
